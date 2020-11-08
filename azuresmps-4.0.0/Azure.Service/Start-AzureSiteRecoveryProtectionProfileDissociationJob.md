---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 185506BC-6155-4517-BCBD-BCDE7450C7A8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8017c2947a8d046226a63b5ed07b3714c35b22c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046410"
---
# <span data-ttu-id="8e1c0-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span><span class="sxs-lookup"><span data-stu-id="8e1c0-101">Start-AzureSiteRecoveryProtectionProfileDissociationJob</span></span>

## <span data-ttu-id="8e1c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1c0-103">사이트 복구 보호 컨테이너와 연결 된 복제 정책에서 dissociation 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-103">Starts a dissociation job on a replication policy associated with a Site Recovery protection container.</span></span>

## <span data-ttu-id="8e1c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e1c0-104">SYNTAX</span></span>

### <span data-ttu-id="8e1c0-105">EnterpriseToAzure (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e1c0-105">EnterpriseToAzure (Default)</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8e1c0-106">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="8e1c0-106">EnterpriseToEnterprise</span></span>
```
Start-AzureSiteRecoveryProtectionProfileDissociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e1c0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8e1c0-107">DESCRIPTION</span></span>
<span data-ttu-id="8e1c0-108">**AzureSiteRecoveryProtectionProfileDissociationJob** Cmdlet은 Azure Site Recovery 보호 컨테이너와 연결 된 복제 정책에서 dissociation 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-108">The **Start-AzureSiteRecoveryProtectionProfileDissociationJob** cmdlet initiates a dissociation job on the replication policy associated with an Azure Site Recovery protection container.</span></span>

## <span data-ttu-id="8e1c0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8e1c0-109">EXAMPLES</span></span>

### <span data-ttu-id="8e1c0-110">예제 1: 보호 프로필 분리</span><span class="sxs-lookup"><span data-stu-id="8e1c0-110">Example 1: Dissociate a protection profile</span></span>
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileDissociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionContainer01.AvailableProtectionProfiles[0] -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-30 02:55:55Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="8e1c0-111">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 보호 컨테이너를 가져온 다음 해당 컨테이너를 $ProtectionContainer 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-111">The first command gets a protection container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that container in the $ProtectionContainer01 variable.</span></span>

<span data-ttu-id="8e1c0-112">두 번째 명령은 보호 컨테이너를 가져온 다음 $ProtectionContainer 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-112">The second command gets a protection container, and then stores it in the $ProtectionContainer02 variable.</span></span>

<span data-ttu-id="8e1c0-113">마지막 명령은 $ProtectionContainer 01에 저장 된 컨테이너의 보호 프로필을 기본 보호 컨테이너로 dissociates.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-113">The final command dissociates the protection profile from the container stored in $ProtectionContainer01 as the primary protection container.</span></span>
<span data-ttu-id="8e1c0-114">이 명령은 $ProtectionContainer 02에 저장 된 컨테이너를 복구 보호 컨테이너로 dissociates.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-114">The command dissociates the container stored in $ProtectionContainer02 as the recovery protection container.</span></span>

## <span data-ttu-id="8e1c0-115">변수</span><span class="sxs-lookup"><span data-stu-id="8e1c0-115">PARAMETERS</span></span>

### <span data-ttu-id="8e1c0-116">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8e1c0-116">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="8e1c0-117">주 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-117">Specifies a primary protection container.</span></span>

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

### <span data-ttu-id="8e1c0-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="8e1c0-118">-Profile</span></span>
<span data-ttu-id="8e1c0-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8e1c0-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e1c0-121">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="8e1c0-121">-ProtectionProfile</span></span>
<span data-ttu-id="8e1c0-122">보호 컨테이너에서 분리할 보호 프로필 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-122">Specifies the protection profile settings to disassociate from the protection containers.</span></span>
<span data-ttu-id="8e1c0-123">보호 컨테이너에 적용할 보호 프로필 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-123">Specifies the protection profile settings to apply to the protection containers.</span></span>
<span data-ttu-id="8e1c0-124">**ASRProtectionProfile** 개체를 가져오려면 New-AzureSiteRecoveryProtectionProfileObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-124">To obtain an **ASRProtectionProfile** object, use the New-AzureSiteRecoveryProtectionProfileObject cmdlet.</span></span>

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

### <span data-ttu-id="8e1c0-125">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8e1c0-125">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="8e1c0-126">복구 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-126">Specifies a recovery protection container.</span></span>

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

### <span data-ttu-id="8e1c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1c0-127">CommonParameters</span></span>
<span data-ttu-id="8e1c0-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e1c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1c0-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1c0-130">입력</span><span class="sxs-lookup"><span data-stu-id="8e1c0-130">INPUTS</span></span>

## <span data-ttu-id="8e1c0-131">출력</span><span class="sxs-lookup"><span data-stu-id="8e1c0-131">OUTPUTS</span></span>

## <span data-ttu-id="8e1c0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8e1c0-132">NOTES</span></span>

## <span data-ttu-id="8e1c0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e1c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="8e1c0-134">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="8e1c0-134">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="8e1c0-135">새로운 AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="8e1c0-135">New-AzureSiteRecoveryProtectionProfileObject</span></span>](./New-AzureSiteRecoveryProtectionProfileObject.md)

[<span data-ttu-id="8e1c0-136">시작-AzureSiteRecoveryProtectionProfileAssociationJob</span><span class="sxs-lookup"><span data-stu-id="8e1c0-136">Start-AzureSiteRecoveryProtectionProfileAssociationJob</span></span>](./Start-AzureSiteRecoveryProtectionProfileAssociationJob.md)


