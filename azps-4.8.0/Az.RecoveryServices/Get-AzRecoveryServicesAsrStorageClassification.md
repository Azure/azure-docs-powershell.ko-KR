---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203788"
---
# <span data-ttu-id="a33b4-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a33b4-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="a33b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a33b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a33b4-103">복구 서비스 자격 증명 모음에서 사용 가능한 (검색 된) ASR 저장소 분류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a33b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a33b4-104">SYNTAX</span></span>

### <span data-ttu-id="a33b4-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a33b4-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a33b4-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a33b4-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a33b4-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a33b4-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33b4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a33b4-108">DESCRIPTION</span></span>
<span data-ttu-id="a33b4-109">**AzRecoveryServicesAsrStorageClassification** Cmdlet은 복구 서비스 자격 증명 모음에 있는 검색 된 ASR 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a33b4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a33b4-110">EXAMPLES</span></span>

### <span data-ttu-id="a33b4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a33b4-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="a33b4-112">지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="a33b4-113">변수</span><span class="sxs-lookup"><span data-stu-id="a33b4-113">PARAMETERS</span></span>

### <span data-ttu-id="a33b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33b4-114">-DefaultProfile</span></span>
<span data-ttu-id="a33b4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a33b4-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="a33b4-116">-Fabric</span></span>
<span data-ttu-id="a33b4-117">ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="a33b4-118">Cmdlet은 지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33b4-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a33b4-119">-FriendlyName</span></span>
<span data-ttu-id="a33b4-120">가져올 저장소 분류 개체의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-120">Specifies the friendly name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33b4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a33b4-121">-Name</span></span>
<span data-ttu-id="a33b4-122">가져올 저장소 분류 개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-122">Specifies the name of the storage classification object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33b4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33b4-123">CommonParameters</span></span>
<span data-ttu-id="a33b4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a33b4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33b4-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a33b4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33b4-126">입력</span><span class="sxs-lookup"><span data-stu-id="a33b4-126">INPUTS</span></span>

### <span data-ttu-id="a33b4-127">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="a33b4-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a33b4-128">출력</span><span class="sxs-lookup"><span data-stu-id="a33b4-128">OUTPUTS</span></span>

### <span data-ttu-id="a33b4-129">SiteRecovery. ASRStorageClassification에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="a33b4-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="a33b4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a33b4-130">NOTES</span></span>

## <span data-ttu-id="a33b4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a33b4-131">RELATED LINKS</span></span>
