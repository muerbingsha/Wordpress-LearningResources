转载地址：http://www.solagirl.net/woocommerce-number-of-products-sold.html

WooCommerce将每个产品的总销量作为wp_postmeta表里，可以用get_post_meta获取，方法如下

在主题的functions.php中加入如下代码




//在shop页面显示总销量
add_action( 'woocommerce_after_shop_loop_item_title', 'wc_product_sold_count', 5 );
//在产品详情页面显示总销量
add_action( 'woocommerce_single_product_summary', 'wc_product_sold_count', 11 );
 
function wc_product_sold_count() {
    global $product;
    $units_sold = get_post_meta( $product->id, 'total_sales', true );
    echo '<p>' . sprintf( __( '已销售: %s', 'woocommerce' ), $units_sold ) . '</p>';
}



修改add_action最后的数字可以调整位置，值越大越靠后。

效果如下所示：

在shop页面显示

product-sold2

在产品详情页面显示

product-sold

WooCommerce只记录了总销量，无法显示月销量。
