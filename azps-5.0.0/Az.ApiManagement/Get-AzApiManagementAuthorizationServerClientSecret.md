---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserverclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServerClientSecret.md
ms.openlocfilehash: 19e49269a4ae07b39e7a2795636e51df75b54905
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309762"
---
# <span data-ttu-id="2e35d-101">Get-AzApiManagementAuthorizationServerClientSecret</span><span class="sxs-lookup"><span data-stu-id="2e35d-101">Get-AzApiManagementAuthorizationServerClientSecret</span></span>

## <span data-ttu-id="2e35d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e35d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e35d-103">API 관리 권한 부여 서버 클라이언트 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-103">Gets an API Management authorization server client secret.</span></span>

## <span data-ttu-id="2e35d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e35d-104">SYNTAX</span></span>

### <span data-ttu-id="2e35d-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e35d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e35d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e35d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServerClientSecret [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e35d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2e35d-107">DESCRIPTION</span></span>
<span data-ttu-id="2e35d-108">**AzApiManagementAuthorizationServerClientSecret** Cmdlet은 Azure API 관리 권한 부여 서버의 클라이언트 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-108">The **Get-AzApiManagementAuthorizationServerClientSecret** cmdlet gets the client secret of the Azure API Management authorization server.</span></span>

## <span data-ttu-id="2e35d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2e35d-109">EXAMPLES</span></span>

### <span data-ttu-id="2e35d-110">예제 1: id를 기준으로 지정 된 권한 부여 서버 클라이언트 암호 가져오기</span><span class="sxs-lookup"><span data-stu-id="2e35d-110">Example 1: Get a specified authorization server client secret by id</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServerClientSecret -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="2e35d-111">이 명령은 지정 된 권한 부여 서버 cient 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-111">This command gets the specified authorization server cient secret.</span></span>

## <span data-ttu-id="2e35d-112">변수</span><span class="sxs-lookup"><span data-stu-id="2e35d-112">PARAMETERS</span></span>

### <span data-ttu-id="2e35d-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2e35d-113">-Context</span></span>
<span data-ttu-id="2e35d-114">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e35d-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2e35d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e35d-116">-DefaultProfile</span></span>
<span data-ttu-id="2e35d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e35d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e35d-118">-ResourceId</span></span>
<span data-ttu-id="2e35d-119">권한 부여 서버의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-119">Arm Resource Identifier of the authorization server.</span></span>
<span data-ttu-id="2e35d-120">지정 된 경우 식별자를 사용 하 여 권한 부여 서버를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-120">If specified will try to find authorization server by the identifier.</span></span>
<span data-ttu-id="2e35d-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="2e35d-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="2e35d-122">-ServerId</span></span>
<span data-ttu-id="2e35d-123">권한 부여 서버의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-123">Identifier of the authorization server.</span></span>
<span data-ttu-id="2e35d-124">지정 된 경우 식별자를 기준으로 권한 부여 서버를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-124">If specified will find authorization server by the identifier.</span></span>
<span data-ttu-id="2e35d-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2e35d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e35d-126">CommonParameters</span></span>
<span data-ttu-id="2e35d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e35d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e35d-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e35d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e35d-129">입력</span><span class="sxs-lookup"><span data-stu-id="2e35d-129">INPUTS</span></span>

### <span data-ttu-id="2e35d-130">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e35d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e35d-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e35d-131">System.String</span></span>

## <span data-ttu-id="2e35d-132">출력</span><span class="sxs-lookup"><span data-stu-id="2e35d-132">OUTPUTS</span></span>

### <span data-ttu-id="2e35d-133">ApiManagement. ServiceManagement. \ PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="2e35d-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="2e35d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2e35d-134">NOTES</span></span>

## <span data-ttu-id="2e35d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e35d-135">RELATED LINKS</span></span>
