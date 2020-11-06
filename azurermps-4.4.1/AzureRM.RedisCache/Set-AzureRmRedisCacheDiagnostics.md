---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 103567021d7317a6777ca5fdb01c53d1f9f023a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536196"
---
# <span data-ttu-id="30eca-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="30eca-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="30eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30eca-102">SYNOPSIS</span></span>
<span data-ttu-id="30eca-103">Azure Redis Cache에 대 한 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30eca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30eca-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30eca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30eca-105">DESCRIPTION</span></span>
<span data-ttu-id="30eca-106">AzureRmRedisCacheDiagnostics cmdlet은 Azure Redis Cache에 대 한 진단을 사용 하도록 **설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="30eca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="30eca-107">EXAMPLES</span></span>

### <span data-ttu-id="30eca-108">예제 1: 진단 사용</span><span class="sxs-lookup"><span data-stu-id="30eca-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="30eca-109">이 명령은 Azure Redis cache에 대 한 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="30eca-110">이 명령은 구독에 대해 동일한 지역에서 모든 Azure Redis 캐시에 대 한 진단 또는 저장소 계정을 업데이트 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="30eca-111">변수</span><span class="sxs-lookup"><span data-stu-id="30eca-111">PARAMETERS</span></span>

### <span data-ttu-id="30eca-112">-이름</span><span class="sxs-lookup"><span data-stu-id="30eca-112">-Name</span></span>
<span data-ttu-id="30eca-113">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-113">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30eca-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30eca-114">-ResourceGroupName</span></span>
<span data-ttu-id="30eca-115">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-115">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30eca-116">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30eca-116">-StorageAccountId</span></span>
<span data-ttu-id="30eca-117">진단 데이터를 저장 하는 데 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-117">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30eca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30eca-118">-DefaultProfile</span></span>
<span data-ttu-id="30eca-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30eca-120">CommonParameters</span></span>
<span data-ttu-id="30eca-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30eca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30eca-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30eca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30eca-123">입력</span><span class="sxs-lookup"><span data-stu-id="30eca-123">INPUTS</span></span>

### <span data-ttu-id="30eca-124">않아야</span><span class="sxs-lookup"><span data-stu-id="30eca-124">None</span></span>

## <span data-ttu-id="30eca-125">출력</span><span class="sxs-lookup"><span data-stu-id="30eca-125">OUTPUTS</span></span>

### <span data-ttu-id="30eca-126">형식이</span><span class="sxs-lookup"><span data-stu-id="30eca-126">Void</span></span>

## <span data-ttu-id="30eca-127">상속자</span><span class="sxs-lookup"><span data-stu-id="30eca-127">NOTES</span></span>
* <span data-ttu-id="30eca-128">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="30eca-128">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="30eca-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30eca-129">RELATED LINKS</span></span>

[<span data-ttu-id="30eca-130">제거-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="30eca-130">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


