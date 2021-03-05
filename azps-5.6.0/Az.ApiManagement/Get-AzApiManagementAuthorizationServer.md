---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 098fb692e1710b9463650f0e398d999f0a2b1062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983771"
---
# <span data-ttu-id="7f136-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f136-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="7f136-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f136-102">SYNOPSIS</span></span>
<span data-ttu-id="7f136-103">API Management 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="7f136-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f136-104">SYNTAX</span></span>

### <span data-ttu-id="7f136-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f136-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f136-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f136-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f136-107">설명</span><span class="sxs-lookup"><span data-stu-id="7f136-107">DESCRIPTION</span></span>
<span data-ttu-id="7f136-108">**Get-AzApiManagementAuthorizationServer** cmdlet은 모든 Azure API Management 권한 부여 서버 또는 지정된 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="7f136-109">ClientSecret은 결과 세부 정보에는 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="7f136-110">클라이언트 비밀을 얻기 위해 **Get-AzApiManagementAuthorizationServerClientSecret** 을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="7f136-111">예제</span><span class="sxs-lookup"><span data-stu-id="7f136-111">EXAMPLES</span></span>

### <span data-ttu-id="7f136-112">예제 1: 모든 권한 부여 서버 사용</span><span class="sxs-lookup"><span data-stu-id="7f136-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="7f136-113">이 명령은 모든 API Management 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="7f136-114">예제 2: 지정된 권한 부여 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="7f136-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="7f136-115">이 명령은 지정된 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="7f136-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f136-116">PARAMETERS</span></span>

### <span data-ttu-id="7f136-117">-Context</span><span class="sxs-lookup"><span data-stu-id="7f136-117">-Context</span></span>

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

### <span data-ttu-id="7f136-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f136-118">-DefaultProfile</span></span>
<span data-ttu-id="7f136-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f136-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f136-120">-ResourceId</span></span>
<span data-ttu-id="7f136-121">권한 부여 서버의 리소스 식별자 팔.</span><span class="sxs-lookup"><span data-stu-id="7f136-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="7f136-122">지정한 경우 식별자에 의해 권한 부여 서버를 찾으려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="7f136-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-123">This parameter is required.</span></span>

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

### <span data-ttu-id="7f136-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="7f136-124">-ServerId</span></span>
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

### <span data-ttu-id="7f136-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f136-125">CommonParameters</span></span>
<span data-ttu-id="7f136-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f136-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f136-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f136-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f136-128">입력</span><span class="sxs-lookup"><span data-stu-id="7f136-128">INPUTS</span></span>

### <span data-ttu-id="7f136-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7f136-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7f136-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7f136-130">System.String</span></span>

## <span data-ttu-id="7f136-131">출력</span><span class="sxs-lookup"><span data-stu-id="7f136-131">OUTPUTS</span></span>

### <span data-ttu-id="7f136-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f136-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="7f136-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f136-133">NOTES</span></span>

## <span data-ttu-id="7f136-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f136-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f136-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f136-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7f136-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f136-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="7f136-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="7f136-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


