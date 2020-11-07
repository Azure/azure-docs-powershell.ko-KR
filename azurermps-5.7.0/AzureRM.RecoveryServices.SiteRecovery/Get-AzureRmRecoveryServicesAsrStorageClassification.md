---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: 8bea83b033ffb8a2e56ba6d28759e88280529a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703246"
---
# <span data-ttu-id="f89fa-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f89fa-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="f89fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f89fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f89fa-103">복구 서비스 자격 증명 모음에서 사용 가능한 (검색 된) ASR 저장소 분류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f89fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f89fa-104">SYNTAX</span></span>

### <span data-ttu-id="f89fa-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="f89fa-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f89fa-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f89fa-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f89fa-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f89fa-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f89fa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f89fa-108">DESCRIPTION</span></span>
<span data-ttu-id="f89fa-109">**AzureRmRecoveryServicesAsrStorageClassification** Cmdlet은 복구 서비스 자격 증명 모음에 있는 검색 된 ASR 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="f89fa-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f89fa-110">EXAMPLES</span></span>

### <span data-ttu-id="f89fa-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f89fa-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="f89fa-112">지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="f89fa-113">변수</span><span class="sxs-lookup"><span data-stu-id="f89fa-113">PARAMETERS</span></span>

### <span data-ttu-id="f89fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f89fa-114">-DefaultProfile</span></span>
<span data-ttu-id="f89fa-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="f89fa-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="f89fa-116">-Fabric</span></span>
<span data-ttu-id="f89fa-117">ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="f89fa-118">Cmdlet은 지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f89fa-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f89fa-119">-FriendlyName</span></span>
<span data-ttu-id="f89fa-120">가져올 저장소 분류 개체의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89fa-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f89fa-121">-Name</span></span>
<span data-ttu-id="f89fa-122">가져올 저장소 분류 개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f89fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f89fa-123">CommonParameters</span></span>
<span data-ttu-id="f89fa-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f89fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f89fa-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f89fa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f89fa-126">입력</span><span class="sxs-lookup"><span data-stu-id="f89fa-126">INPUTS</span></span>

### <span data-ttu-id="f89fa-127">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="f89fa-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="f89fa-128">출력</span><span class="sxs-lookup"><span data-stu-id="f89fa-128">OUTPUTS</span></span>

### <span data-ttu-id="f89fa-129">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRStorageClassification, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="f89fa-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f89fa-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f89fa-130">NOTES</span></span>

## <span data-ttu-id="f89fa-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f89fa-131">RELATED LINKS</span></span>
