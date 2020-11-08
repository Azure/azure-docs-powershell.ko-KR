---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CE15E01D-5D86-4960-8E37-7757B35F4464
online version: ''
schema: 2.0.0
ms.openlocfilehash: a87a825249d7d7cda3fc2dc43a93869f8d869705
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046569"
---
# <span data-ttu-id="d2c3d-101">Get-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="d2c3d-101">Get-AzureSiteRecoveryVM</span></span>

## <span data-ttu-id="d2c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c3d-103">사이트 복구 관리 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-103">Gets information about Site Recovery-managed virtual machines.</span></span>

## <span data-ttu-id="d2c3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2c3d-104">SYNTAX</span></span>

### <span data-ttu-id="d2c3d-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2c3d-105">ByObject (Default)</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c3d-106">ByObjectWithId</span><span class="sxs-lookup"><span data-stu-id="d2c3d-106">ByObjectWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c3d-107">ByIDsWithId</span><span class="sxs-lookup"><span data-stu-id="d2c3d-107">ByIDsWithId</span></span>
```
Get-AzureSiteRecoveryVM -Id <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c3d-108">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d2c3d-108">ByObjectWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d2c3d-109">ByIDsWithName</span><span class="sxs-lookup"><span data-stu-id="d2c3d-109">ByIDsWithName</span></span>
```
Get-AzureSiteRecoveryVM -Name <String> -ProtectionContainerId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2c3d-110">ByIDs</span><span class="sxs-lookup"><span data-stu-id="d2c3d-110">ByIDs</span></span>
```
Get-AzureSiteRecoveryVM -ProtectionContainerId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d2c3d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="d2c3d-111">DESCRIPTION</span></span>
<span data-ttu-id="d2c3d-112">**AzureSiteRecoveryVM** Cmdlet은 Azure Site Recovery에서 관리 되는 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-112">The **Get-AzureSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="d2c3d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d2c3d-113">EXAMPLES</span></span>

### <span data-ttu-id="d2c3d-114">예제 1: 가상 컴퓨터에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2c3d-114">Example 1: Get information about a virtual machine</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> Get-AzureSiteRecoveryVM -ProtectionContainer $ProtectionContainer
ID                          : a205fd17-3848-4896-bab6-9dbccc3cd8ed
ServerId                    : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c
ProtectionContainerId       : 4a94c4a9-c856-4577-afbd-367fe9b3ce9c_1c513d45-645d-4ed0-b9ae-e7b869a1f7fc
Name                        : vm1
Type                        : VirtualMachine
FabricObjectId              : 86447b9e-d877-4e9a-8302-adcd6bbf18c0
Protected                   : False
CanCommit                   : False
CanFailover                 : True
CanReverseReplicate         : False
ActiveLocation              : Primary
ProtectionState             : Enabled
ReplicationHealth           : Healthy
TestFailoverState           : None
ReplicationProvider         : HyperVReplica
```

<span data-ttu-id="d2c3d-115">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 protected 컨테이너를 얻은 다음 $ProtectionContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-115">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="d2c3d-116">두 번째 명령은 $ProtectionContainer의 가상 컴퓨터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-116">The second command gets information about the virtual machines in $ProtectionContainer.</span></span>

## <span data-ttu-id="d2c3d-117">변수</span><span class="sxs-lookup"><span data-stu-id="d2c3d-117">PARAMETERS</span></span>

### <span data-ttu-id="d2c3d-118">-Id</span><span class="sxs-lookup"><span data-stu-id="d2c3d-118">-Id</span></span>
<span data-ttu-id="d2c3d-119">정보를 가져올 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-119">Specifies the ID of the virtual machine about which to get information.</span></span>

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

### <span data-ttu-id="d2c3d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d2c3d-120">-Name</span></span>
<span data-ttu-id="d2c3d-121">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-121">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d2c3d-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="d2c3d-122">-Profile</span></span>
<span data-ttu-id="d2c3d-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2c3d-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2c3d-125">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d2c3d-125">-ProtectionContainer</span></span>
<span data-ttu-id="d2c3d-126">사이트 복구 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-126">Specifies the Site Recovery protection container object.</span></span>

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

### <span data-ttu-id="d2c3d-127">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="d2c3d-127">-ProtectionContainerId</span></span>
<span data-ttu-id="d2c3d-128">정보를 가져올 보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-128">Specifies the ID of a protected container about which to get information.</span></span>

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

### <span data-ttu-id="d2c3d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c3d-129">CommonParameters</span></span>
<span data-ttu-id="d2c3d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2c3d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c3d-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c3d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c3d-132">입력</span><span class="sxs-lookup"><span data-stu-id="d2c3d-132">INPUTS</span></span>

## <span data-ttu-id="d2c3d-133">출력</span><span class="sxs-lookup"><span data-stu-id="d2c3d-133">OUTPUTS</span></span>

## <span data-ttu-id="d2c3d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d2c3d-134">NOTES</span></span>

## <span data-ttu-id="d2c3d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2c3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2c3d-136">Set-AzureSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="d2c3d-136">Set-AzureSiteRecoveryVM</span></span>](./Set-AzureSiteRecoveryVM.md)


