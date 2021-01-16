---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366136"
---
# <span data-ttu-id="e811f-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="e811f-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="e811f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e811f-102">SYNOPSIS</span></span>
<span data-ttu-id="e811f-103">API Management 권한 부여 서버 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="e811f-104">구문</span><span class="sxs-lookup"><span data-stu-id="e811f-104">SYNTAX</span></span>

### <span data-ttu-id="e811f-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e811f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e811f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e811f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e811f-107">설명</span><span class="sxs-lookup"><span data-stu-id="e811f-107">DESCRIPTION</span></span>
<span data-ttu-id="e811f-108">**Get-AzApiManagementAuthorizationServerClientSecret** cmdlet은 Azure API Management 권한 부여 서버의 클라이언트 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="e811f-109">예제</span><span class="sxs-lookup"><span data-stu-id="e811f-109">EXAMPLES</span></span>

### <span data-ttu-id="e811f-110">예제 1: ID로 지정된 권한 부여 서버 클라이언트 비밀을 얻게</span><span class="sxs-lookup"><span data-stu-id="e811f-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="e811f-111">이 명령은 지정된 권한 부여 서버 cient 비밀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="e811f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e811f-112">PARAMETERS</span></span>

### <span data-ttu-id="e811f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="e811f-113">-Context</span></span>
<span data-ttu-id="e811f-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e811f-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-115">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e811f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e811f-116">-DefaultProfile</span></span>
<span data-ttu-id="e811f-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e811f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e811f-118">-ResourceId</span></span>
<span data-ttu-id="e811f-119">권한 부여 서버의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="e811f-120">지정된 경우 식별자에 의해 권한 부여 서버를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="e811f-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e811f-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e811f-122">-ServerId</span></span>
<span data-ttu-id="e811f-123">권한 부여 서버의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="e811f-124">지정된 경우 식별자에 의해 권한 부여 서버를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="e811f-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e811f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e811f-126">CommonParameters</span></span>
<span data-ttu-id="e811f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e811f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e811f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e811f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e811f-129">입력</span><span class="sxs-lookup"><span data-stu-id="e811f-129">INPUTS</span></span>

### <span data-ttu-id="e811f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e811f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e811f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e811f-131">System.String</span></span>

## <span data-ttu-id="e811f-132">출력</span><span class="sxs-lookup"><span data-stu-id="e811f-132">OUTPUTS</span></span>

### <span data-ttu-id="e811f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="e811f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="e811f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e811f-134">NOTES</span></span>

## <span data-ttu-id="e811f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e811f-135">RELATED LINKS</span></span>
