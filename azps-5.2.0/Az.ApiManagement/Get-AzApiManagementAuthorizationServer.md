---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338793"
---
# <span data-ttu-id="4a4f6-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a4f6-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="4a4f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4a4f6-103">API Management 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="4a4f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a4f6-104">SYNTAX</span></span>

### <span data-ttu-id="4a4f6-105">ContextParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4a4f6-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a4f6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a4f6-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a4f6-107">설명</span><span class="sxs-lookup"><span data-stu-id="4a4f6-107">DESCRIPTION</span></span>
<span data-ttu-id="4a4f6-108">**Get-AzApiManagementAuthorizationServer** cmdlet은 모든 Azure API Management 권한 부여 서버 또는 지정된 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="4a4f6-109">ClientSecret은 결과 세부 정보에 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="4a4f6-110">클라이언트 비밀을 얻습니다. **Get-AzApiManagementAuthorizationServerClientSecret을 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="4a4f6-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="4a4f6-111">예제</span><span class="sxs-lookup"><span data-stu-id="4a4f6-111">EXAMPLES</span></span>

### <span data-ttu-id="4a4f6-112">예제 1: 모든 권한 부여 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="4a4f6-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="4a4f6-113">이 명령은 모든 API Management 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="4a4f6-114">예제 2: 지정된 권한 부여 서버 얻기</span><span class="sxs-lookup"><span data-stu-id="4a4f6-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="4a4f6-115">이 명령은 지정된 권한 부여 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="4a4f6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a4f6-116">PARAMETERS</span></span>

### <span data-ttu-id="4a4f6-117">-Context</span><span class="sxs-lookup"><span data-stu-id="4a4f6-117">-Context</span></span>

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

### <span data-ttu-id="4a4f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a4f6-118">-DefaultProfile</span></span>
<span data-ttu-id="4a4f6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a4f6-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a4f6-120">-ResourceId</span></span>
<span data-ttu-id="4a4f6-121">권한 부여 서버의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="4a4f6-122">지정된 경우 식별자에 의해 권한 부여 서버를 찾으려고 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="4a4f6-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-123">This parameter is required.</span></span>

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

### <span data-ttu-id="4a4f6-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="4a4f6-124">-ServerId</span></span>
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

### <span data-ttu-id="4a4f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a4f6-125">CommonParameters</span></span>
<span data-ttu-id="4a4f6-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a4f6-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4a4f6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a4f6-128">입력</span><span class="sxs-lookup"><span data-stu-id="4a4f6-128">INPUTS</span></span>

### <span data-ttu-id="4a4f6-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4a4f6-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4a4f6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4a4f6-130">System.String</span></span>

## <span data-ttu-id="4a4f6-131">출력</span><span class="sxs-lookup"><span data-stu-id="4a4f6-131">OUTPUTS</span></span>

### <span data-ttu-id="4a4f6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a4f6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="4a4f6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a4f6-133">NOTES</span></span>

## <span data-ttu-id="4a4f6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a4f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a4f6-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a4f6-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4a4f6-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a4f6-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="4a4f6-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="4a4f6-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


