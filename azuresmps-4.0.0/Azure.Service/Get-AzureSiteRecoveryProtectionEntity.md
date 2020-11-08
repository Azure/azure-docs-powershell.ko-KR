---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB1A36E9-75BE-43CF-9092-9713DFEB96F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5329d50f87b92254136c222f406bb49586d6d7a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045588"
---
# <span data-ttu-id="7d394-101">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7d394-101">Get-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="7d394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d394-102">SYNOPSIS</span></span>
<span data-ttu-id="7d394-103">사이트 복구 자격 증명 모음에서 보호 가능한 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-103">Gets protectable or protected entities in a Site Recovery vault.</span></span>

## <span data-ttu-id="7d394-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d394-104">SYNTAX</span></span>

### <span data-ttu-id="7d394-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d394-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d394-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="7d394-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d394-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="7d394-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d394-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7d394-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d394-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="7d394-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -Name <String> -ProtectionContainerId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d394-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="7d394-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryProtectionEntity -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d394-111">설명은</span><span class="sxs-lookup"><span data-stu-id="7d394-111">DESCRIPTION</span></span>
<span data-ttu-id="7d394-112">**AzureSiteRecoveryProtectionEntity** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 있는 가상 컴퓨터와 같은 보호 가능한 엔터티나 protected 엔터티를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-112">The **Get-AzureSiteRecoveryProtectionEntity** cmdlet gets the protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7d394-113">예제의</span><span class="sxs-lookup"><span data-stu-id="7d394-113">EXAMPLES</span></span>

### <span data-ttu-id="7d394-114">예제 1: 컨테이너에 보호 된 가상 컴퓨터 표시</span><span class="sxs-lookup"><span data-stu-id="7d394-114">Example 1: Display a protected virtual machine in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
ID                           : 43aaab46-1cb0-4c39-8077-9a091c3b05ce
ServerId                     : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId        : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                         : testvm
Type                         : VirtualMachine
FabricObjectId               : 506B3CAC-5758-49E2-98C4-E5B0512E4D8E
Protected                    : False
CanCommit                    : False
CanFailover                  : False
CanReverseReplicate          : False
ActiveLocation               : Primary
ProtectionStateDescription   : Enabling protection
ReplicationHealth            : 
TestFailoverStateDescription : Nonev
ReplicationProvider          : HyperVReplica
```

<span data-ttu-id="7d394-115">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 보호 된 컨테이너를 가져온 다음 해당 개체를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-115">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="7d394-116">두 번째 명령은 $Container의 컨테이너에 속하는 보호 된 가상 컴퓨터를 가져온 다음 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-116">The second command gets the protected virtual machine that belongs to the container in $Container, and then displays it.</span></span>

## <span data-ttu-id="7d394-117">변수</span><span class="sxs-lookup"><span data-stu-id="7d394-117">PARAMETERS</span></span>

### <span data-ttu-id="7d394-118">-Id</span><span class="sxs-lookup"><span data-stu-id="7d394-118">-Id</span></span>
<span data-ttu-id="7d394-119">가져올 보호 엔터티의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-119">Specifies the ID of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithId, ByIDsWithId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d394-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7d394-120">-Name</span></span>
<span data-ttu-id="7d394-121">가져올 보호 엔터티의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-121">Specifies the name of a protection entity to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByIDsWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d394-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="7d394-122">-Profile</span></span>
<span data-ttu-id="7d394-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d394-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d394-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d394-125">-ProtectionContainer</span></span>
<span data-ttu-id="7d394-126">보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-126">Specifies a protection container.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithId, ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d394-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="7d394-127">-ProtectionContainerId</span></span>
<span data-ttu-id="7d394-128">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-128">Specifies the ID of a protected container.</span></span>

```yaml
Type: String
Parameter Sets: ByIDsWithId, ByIDsWithName, ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d394-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d394-129">CommonParameters</span></span>
<span data-ttu-id="7d394-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d394-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d394-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d394-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d394-132">입력</span><span class="sxs-lookup"><span data-stu-id="7d394-132">INPUTS</span></span>

## <span data-ttu-id="7d394-133">출력</span><span class="sxs-lookup"><span data-stu-id="7d394-133">OUTPUTS</span></span>

## <span data-ttu-id="7d394-134">상속자</span><span class="sxs-lookup"><span data-stu-id="7d394-134">NOTES</span></span>

## <span data-ttu-id="7d394-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d394-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d394-136">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7d394-136">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7d394-137">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7d394-137">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="7d394-138">업데이트-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7d394-138">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


