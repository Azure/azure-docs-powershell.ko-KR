---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045848"
---
# <span data-ttu-id="7d782-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="7d782-101">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>

## <span data-ttu-id="7d782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d782-102">SYNOPSIS</span></span>
<span data-ttu-id="7d782-103">사이트 복구 복제 정책 연결 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-103">Starts a Site Recovery replication policy association job.</span></span>

## <span data-ttu-id="7d782-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d782-104">SYNTAX</span></span>

### <span data-ttu-id="7d782-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d782-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d782-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="7d782-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d782-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d782-107">DESCRIPTION</span></span>
<span data-ttu-id="7d782-108">**AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet은 복제 정책을 Azure Site Recovery 보호 컨테이너와 연결 하는 연결 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-108">The **Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet initiates an association job to associate a replication policy with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="7d782-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d782-109">EXAMPLES</span></span>

### <span data-ttu-id="7d782-110">예제 1: 보호 프로필 연결</span><span class="sxs-lookup"><span data-stu-id="7d782-110">Example 1: Associate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

<span data-ttu-id="7d782-111">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 보호 컨테이너를 가져온 다음 해당 컨테이너를 $ProtectionContainer 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="7d782-112">두 번째 명령은 **새 AzureSiteRecoveryProtectionProfileObject** cmdlet을 사용 하 여 보호 프로필을 만들고 해당 보호 프로필을 $ProtectionProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-112">The second command creates a protection profile by using the **New-AzureSiteRecoveryProtectionProfileObject** cmdlet, and stores that protection profile in the $ProtectionProfile variable.</span></span>

<span data-ttu-id="7d782-113">세 번째 명령은 보호 컨테이너를 가져온 다음 $ProtectionContainer 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-113">The third command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="7d782-114">마지막 명령은 $ProtectionProfile에 저장 된 보호 프로필을 $ProtectionContainer 01에 저장 되어 있는 컨테이너에 기본 보호 컨테이너로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-114">The final command associates the protection profile stored in $ProtectionProfile to the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="7d782-115">이 명령은 $ProtectionContainer 02에 저장 된 컨테이너를 복구 보호 컨테이너로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-115">The command associates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="7d782-116">변수</span><span class="sxs-lookup"><span data-stu-id="7d782-116">PARAMETERS</span></span>

### <span data-ttu-id="7d782-117">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d782-117">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="7d782-118">보호 프로필 설정을 적용할 기본 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-118">Specifies the primary protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d782-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="7d782-119">-Profile</span></span>
<span data-ttu-id="7d782-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d782-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d782-122">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="7d782-122">-ProtectionProfile</span></span>
<span data-ttu-id="7d782-123">보호 컨테이너에 적용할 보호 프로필 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="7d782-124">**ASRProtectionProfile** 개체를 가져오려면 New-AzureSiteRecoveryProtectionProfileObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d782-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d782-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="7d782-126">보호 프로필 설정을 적용할 복구 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-126">Specifies the recovery protection container on which to apply the protection profile settings.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d782-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d782-127">CommonParameters</span></span>
<span data-ttu-id="7d782-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d782-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d782-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d782-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d782-130">입력</span><span class="sxs-lookup"><span data-stu-id="7d782-130">INPUTS</span></span>

## <span data-ttu-id="7d782-131">출력</span><span class="sxs-lookup"><span data-stu-id="7d782-131">OUTPUTS</span></span>

## <span data-ttu-id="7d782-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7d782-132">NOTES</span></span>

## <span data-ttu-id="7d782-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d782-133">RELATED LINKS</span></span>

[<span data-ttu-id="7d782-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d782-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7d782-135">새로운 AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="7d782-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="7d782-136">시작-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="7d782-136">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


