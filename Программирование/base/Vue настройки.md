# Чтобы работал SCSS в Vue
Чтобы в проекте Vue работал #scss нужно:
1. Добавить файл style.scss в папку assets. 
2. Добавить файл vue.config.js в корень проекта.
3. В данном файле написать: 

		module.exports = {  
			 css: {  
				loaderOptions: {  
					sass: {  
						prependData: '@import "@/assets/style.scss";'  
					 }  
				} 
			}
		}
1. Установить node-sass, ass-loader.

ГОТОВО.