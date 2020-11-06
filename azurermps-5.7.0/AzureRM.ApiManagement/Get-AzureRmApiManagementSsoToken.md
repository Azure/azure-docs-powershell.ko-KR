---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529961"
---
# <span data-ttu-id="28bf3-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="28bf3-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="28bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="28bf3-103">SSO 토큰과 API Management 서비스의 배포 된 관리 포털에 대 한 링크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28bf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28bf3-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28bf3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="28bf3-106">**AzureRmApiManagementSsoToken** CMDLET은 SSO (single sign-on) 토큰이 포함 된 링크 (URL)를 API management 서비스의 배포 된 관리 포털에 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="28bf3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="28bf3-108">예제 1: API Management 서비스의 SSO 토큰 가져오기</span><span class="sxs-lookup"><span data-stu-id="28bf3-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="28bf3-109">이 명령은 API Management 서비스의 SSO 토큰을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="28bf3-110">변수</span><span class="sxs-lookup"><span data-stu-id="28bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="28bf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28bf3-111">-DefaultProfile</span></span>
<span data-ttu-id="28bf3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28bf3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="28bf3-113">-Name</span></span>
<span data-ttu-id="28bf3-114">API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-114">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28bf3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28bf3-115">-ResourceGroupName</span></span>
<span data-ttu-id="28bf3-116">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-116">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28bf3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bf3-117">CommonParameters</span></span>
<span data-ttu-id="28bf3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bf3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28bf3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bf3-120">입력</span><span class="sxs-lookup"><span data-stu-id="28bf3-120">INPUTS</span></span>

### <span data-ttu-id="28bf3-121">않아야</span><span class="sxs-lookup"><span data-stu-id="28bf3-121">None</span></span>
<span data-ttu-id="28bf3-122">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28bf3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28bf3-123">출력</span><span class="sxs-lookup"><span data-stu-id="28bf3-123">OUTPUTS</span></span>

### <span data-ttu-id="28bf3-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28bf3-124">System.String</span></span>

## <span data-ttu-id="28bf3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="28bf3-125">NOTES</span></span>

## <span data-ttu-id="28bf3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28bf3-126">RELATED LINKS</span></span>

[<span data-ttu-id="28bf3-127">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="28bf3-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


