---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529096"
---
# <span data-ttu-id="f4363-101">Update-AzureRmSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="f4363-101">Update-AzureRmSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="f4363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4363-102">SYNOPSIS</span></span>
<span data-ttu-id="f4363-103">사이트 복구 개체의 보호를 위해 원본 및 대상 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4363-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4363-104">SYNTAX</span></span>

### <span data-ttu-id="f4363-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4363-105">ByPEObject (Default)</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4363-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="f4363-106">ByRPObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4363-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="f4363-107">ByRPIObject</span></span>
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4363-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f4363-108">DESCRIPTION</span></span>
<span data-ttu-id="f4363-109">**AzureRmSiteRecoveryProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 Azure Site Recovery 개체의 보호를 위해 원본 및 대상 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-109">The **Update-AzureRmSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="f4363-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f4363-110">EXAMPLES</span></span>

## <span data-ttu-id="f4363-111">변수</span><span class="sxs-lookup"><span data-stu-id="f4363-111">PARAMETERS</span></span>

### <span data-ttu-id="f4363-112">방향</span><span class="sxs-lookup"><span data-stu-id="f4363-112">-Direction</span></span>
<span data-ttu-id="f4363-113">커밋 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-113">Specifies the direction of the commit.</span></span>
<span data-ttu-id="f4363-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4363-115">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="f4363-115">PrimaryToRecovery</span></span>
- <span data-ttu-id="f4363-116">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="f4363-116">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4363-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4363-117">-ProtectionEntity</span></span>
<span data-ttu-id="f4363-118">보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-118">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4363-119">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4363-119">-RecoveryPlan</span></span>
<span data-ttu-id="f4363-120">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-120">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4363-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f4363-121">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4363-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4363-122">-DefaultProfile</span></span>
<span data-ttu-id="f4363-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4363-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4363-124">CommonParameters</span></span>
<span data-ttu-id="f4363-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4363-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4363-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4363-127">입력</span><span class="sxs-lookup"><span data-stu-id="f4363-127">INPUTS</span></span>

### <span data-ttu-id="f4363-128">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="f4363-128">ASRProtectionEntity</span></span>
<span data-ttu-id="f4363-129">' ProtectionEntity ' 매개 변수는 파이프라인에서 ' ASRProtectionEntity ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-129">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="f4363-130">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f4363-130">ASRRecoveryPlan</span></span>
<span data-ttu-id="f4363-131">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-131">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="f4363-132">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f4363-132">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f4363-133">' ReplicationProtectedItem ' 매개 변수는 파이프라인에서 ' ASRReplicationProtectedItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4363-133">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f4363-134">출력</span><span class="sxs-lookup"><span data-stu-id="f4363-134">OUTPUTS</span></span>

### <span data-ttu-id="f4363-135">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="f4363-135">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f4363-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f4363-136">NOTES</span></span>

## <span data-ttu-id="f4363-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4363-137">RELATED LINKS</span></span>

