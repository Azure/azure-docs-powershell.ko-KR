---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494431"
---
# <span data-ttu-id="29d9e-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="29d9e-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="29d9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="29d9e-103">API Management 서비스의 배포된 관리 포털에 SSO 토큰이 있는 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="29d9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="29d9e-104">SYNTAX</span></span>

### <span data-ttu-id="29d9e-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="29d9e-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d9e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="29d9e-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29d9e-107">설명</span><span class="sxs-lookup"><span data-stu-id="29d9e-107">DESCRIPTION</span></span>
<span data-ttu-id="29d9e-108">**Get-AzApiManagementSsoToken** cmdlet은 SSO(Single Sign-On) 토큰을 포함하는 링크(URL)를 API Management 서비스의 배포된 관리 포털에 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="29d9e-109">예제</span><span class="sxs-lookup"><span data-stu-id="29d9e-109">EXAMPLES</span></span>

### <span data-ttu-id="29d9e-110">예제 1: API Management 서비스의 SSO 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="29d9e-111">이 명령은 API Management 서비스의 SSO 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="29d9e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29d9e-112">PARAMETERS</span></span>

### <span data-ttu-id="29d9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d9e-113">-DefaultProfile</span></span>
<span data-ttu-id="29d9e-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29d9e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29d9e-115">-InputObject</span></span>
<span data-ttu-id="29d9e-116">PsApiManagement의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="29d9e-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29d9e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="29d9e-118">-Name</span></span>
<span data-ttu-id="29d9e-119">API Management 인스턴스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d9e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d9e-120">-ResourceGroupName</span></span>
<span data-ttu-id="29d9e-121">API Management가 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29d9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d9e-122">CommonParameters</span></span>
<span data-ttu-id="29d9e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29d9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d9e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29d9e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d9e-125">입력</span><span class="sxs-lookup"><span data-stu-id="29d9e-125">INPUTS</span></span>

### <span data-ttu-id="29d9e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="29d9e-126">System.String</span></span>

## <span data-ttu-id="29d9e-127">출력</span><span class="sxs-lookup"><span data-stu-id="29d9e-127">OUTPUTS</span></span>

### <span data-ttu-id="29d9e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="29d9e-128">System.String</span></span>

## <span data-ttu-id="29d9e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29d9e-129">NOTES</span></span>

## <span data-ttu-id="29d9e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29d9e-130">RELATED LINKS</span></span>

[<span data-ttu-id="29d9e-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="29d9e-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


