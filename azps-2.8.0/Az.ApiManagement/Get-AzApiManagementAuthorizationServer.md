---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698122"
---
# <span data-ttu-id="59fa7-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59fa7-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="59fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="59fa7-103">API 관리 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="59fa7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59fa7-104">SYNTAX</span></span>

### <span data-ttu-id="59fa7-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="59fa7-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59fa7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fa7-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fa7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="59fa7-108">**AzApiManagementAuthorizationServer** cmdlet은 모든 Azure API Management 권한 부여 서버 또는 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="59fa7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="59fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="59fa7-110">예제 1: 모든 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fa7-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="59fa7-111">이 명령은 모든 API Management 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="59fa7-112">예제 2: 지정 된 권한 부여 서버 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fa7-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="59fa7-113">이 명령은 지정 된 권한 부여 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="59fa7-114">변수</span><span class="sxs-lookup"><span data-stu-id="59fa7-114">PARAMETERS</span></span>

### <span data-ttu-id="59fa7-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="59fa7-115">-Context</span></span>

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

### <span data-ttu-id="59fa7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fa7-116">-DefaultProfile</span></span>
<span data-ttu-id="59fa7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59fa7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59fa7-118">-ResourceId</span></span>
<span data-ttu-id="59fa7-119">권한 부여 서버의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="59fa7-120">지정 된 경우 식별자를 사용 하 여 권한 부여 서버를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="59fa7-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-121">This parameter is required.</span></span>

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

### <span data-ttu-id="59fa7-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="59fa7-122">-ServerId</span></span>
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

### <span data-ttu-id="59fa7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fa7-123">CommonParameters</span></span>
<span data-ttu-id="59fa7-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fa7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fa7-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59fa7-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fa7-126">입력</span><span class="sxs-lookup"><span data-stu-id="59fa7-126">INPUTS</span></span>

### <span data-ttu-id="59fa7-127">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="59fa7-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="59fa7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59fa7-128">System.String</span></span>

## <span data-ttu-id="59fa7-129">출력</span><span class="sxs-lookup"><span data-stu-id="59fa7-129">OUTPUTS</span></span>

### <span data-ttu-id="59fa7-130">ApiManagement. ServiceManagement. \ PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59fa7-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="59fa7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="59fa7-131">NOTES</span></span>

## <span data-ttu-id="59fa7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59fa7-132">RELATED LINKS</span></span>

[<span data-ttu-id="59fa7-133">새로운 AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59fa7-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="59fa7-134">제거-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59fa7-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="59fa7-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="59fa7-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


