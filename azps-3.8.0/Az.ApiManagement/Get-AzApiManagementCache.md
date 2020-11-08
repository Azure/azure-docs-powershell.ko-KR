---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041942"
---
# <span data-ttu-id="46736-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="46736-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="46736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46736-102">SYNOPSIS</span></span>
<span data-ttu-id="46736-103">캐시에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46736-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="46736-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46736-104">SYNTAX</span></span>

### <span data-ttu-id="46736-105">ContextParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="46736-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46736-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46736-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46736-107">설명은</span><span class="sxs-lookup"><span data-stu-id="46736-107">DESCRIPTION</span></span>
<span data-ttu-id="46736-108">Api Management 서비스에 구성 된 캐시에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46736-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="46736-109">예제의</span><span class="sxs-lookup"><span data-stu-id="46736-109">EXAMPLES</span></span>

### <span data-ttu-id="46736-110">예제 1: 모든 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="46736-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="46736-111">Api Management 서비스에 구성 된 모든 캐시의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46736-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="46736-112">예제 2: 식별자 westus에 지정 된 캐시 가져오기</span><span class="sxs-lookup"><span data-stu-id="46736-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="46736-113">Westus에 대해 구성 된 지정 된 캐시에 대 한 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="46736-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="46736-114">변수</span><span class="sxs-lookup"><span data-stu-id="46736-114">PARAMETERS</span></span>

### <span data-ttu-id="46736-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="46736-115">-CacheId</span></span>
<span data-ttu-id="46736-116">캐시의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-116">Identifier of a cache.</span></span>
<span data-ttu-id="46736-117">지정 된 경우 식별자를 기준으로 캐시를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="46736-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="46736-118">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46736-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="46736-119">-Context</span></span>
<span data-ttu-id="46736-120">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="46736-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46736-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46736-122">-DefaultProfile</span></span>
<span data-ttu-id="46736-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46736-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46736-124">-ResourceId</span></span>
<span data-ttu-id="46736-125">캐시의 Arm 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="46736-126">지정 된 경우 식별자를 기준으로 캐시를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="46736-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="46736-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="46736-127">This parameter is required.</span></span>

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

### <span data-ttu-id="46736-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46736-128">CommonParameters</span></span>
<span data-ttu-id="46736-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46736-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46736-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46736-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46736-131">입력</span><span class="sxs-lookup"><span data-stu-id="46736-131">INPUTS</span></span>

### <span data-ttu-id="46736-132">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46736-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46736-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46736-133">System.String</span></span>

## <span data-ttu-id="46736-134">출력</span><span class="sxs-lookup"><span data-stu-id="46736-134">OUTPUTS</span></span>

### <span data-ttu-id="46736-135">ApiManagement. ServiceManagement. \ PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="46736-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="46736-136">상속자</span><span class="sxs-lookup"><span data-stu-id="46736-136">NOTES</span></span>

## <span data-ttu-id="46736-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46736-137">RELATED LINKS</span></span>

[<span data-ttu-id="46736-138">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="46736-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="46736-139">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="46736-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="46736-140">제거-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="46736-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)