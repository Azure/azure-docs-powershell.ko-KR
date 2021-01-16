---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: a5265f6c824160ccd06022d54613818131f4da94
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493339"
---
# <span data-ttu-id="e9eec-101">Get-AzRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e9eec-101">Get-AzRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="e9eec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9eec-102">SYNOPSIS</span></span>
<span data-ttu-id="e9eec-103">Recovery Services 자격 증명 모음에서 사용 가능한(검색된) ASR 저장소 분류를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e9eec-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9eec-104">SYNTAX</span></span>

### <span data-ttu-id="e9eec-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9eec-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9eec-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e9eec-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9eec-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e9eec-107">ByObjectWithFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9eec-108">설명</span><span class="sxs-lookup"><span data-stu-id="e9eec-108">DESCRIPTION</span></span>
<span data-ttu-id="e9eec-109">**Get-AzRecoveryServicesAsrStorageClassification** cmdlet은 Recovery Services 자격 증명 모음에서 검색된 ASR 저장소 분류에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-109">The **Get-AzRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="e9eec-110">예제</span><span class="sxs-lookup"><span data-stu-id="e9eec-110">EXAMPLES</span></span>

### <span data-ttu-id="e9eec-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9eec-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="e9eec-112">지정된 ASR 패브릭에 해당하는 검색된 저장소 분류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="e9eec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9eec-113">PARAMETERS</span></span>

### <span data-ttu-id="e9eec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9eec-114">-DefaultProfile</span></span>
<span data-ttu-id="e9eec-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e9eec-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="e9eec-116">-Fabric</span></span>
<span data-ttu-id="e9eec-117">ASR 패브릭 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-117">Specifies an ASR fabric object.</span></span> <span data-ttu-id="e9eec-118">cmdlet은 지정된 ASR 패브릭에 해당하는 검색된 저장소 분류의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-118">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="e9eec-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e9eec-119">-FriendlyName</span></span>
<span data-ttu-id="e9eec-120">얻을 저장소 분류 개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-120">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="e9eec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e9eec-121">-Name</span></span>
<span data-ttu-id="e9eec-122">얻을 저장소 분류 개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-122">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="e9eec-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9eec-123">CommonParameters</span></span>
<span data-ttu-id="e9eec-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9eec-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9eec-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9eec-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9eec-126">입력</span><span class="sxs-lookup"><span data-stu-id="e9eec-126">INPUTS</span></span>

### <span data-ttu-id="e9eec-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e9eec-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e9eec-128">출력</span><span class="sxs-lookup"><span data-stu-id="e9eec-128">OUTPUTS</span></span>

### <span data-ttu-id="e9eec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e9eec-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="e9eec-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9eec-130">NOTES</span></span>

## <span data-ttu-id="e9eec-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9eec-131">RELATED LINKS</span></span>
