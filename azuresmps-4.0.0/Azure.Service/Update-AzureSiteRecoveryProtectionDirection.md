---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 870EE77E-57D9-4B52-9F80-CB24D642E6E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f94d95b40fb89f0c1df89ad0c8a9b78eb283184
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046400"
---
# <span data-ttu-id="28543-101">Update-AzureSiteRecoveryProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="28543-101">Update-AzureSiteRecoveryProtectionDirection</span></span>

## <span data-ttu-id="28543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28543-102">SYNOPSIS</span></span>
<span data-ttu-id="28543-103">사이트 복구 개체의 보호를 위해 원본 및 대상 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-103">Updates the source and target server for the protection of a Site Recovery object.</span></span>

## <span data-ttu-id="28543-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28543-104">SYNTAX</span></span>

### <span data-ttu-id="28543-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="28543-105">ByRPObject (Default)</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="28543-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="28543-106">ByRPId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="28543-107">ByPEId</span><span class="sxs-lookup"><span data-stu-id="28543-107">ByPEId</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="28543-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="28543-108">ByPEObject</span></span>
```
Update-AzureSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28543-109">설명은</span><span class="sxs-lookup"><span data-stu-id="28543-109">DESCRIPTION</span></span>
<span data-ttu-id="28543-110">**업데이트 AzureSiteRecoveryProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 Azure Site Recovery 개체의 보호를 위해 원본 및 대상 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-110">The **Update-AzureSiteRecoveryProtectionDirection** cmdlet updates the source and target server for the protection of an Azure Site Recovery object after a commit failover operation finishes.</span></span>

## <span data-ttu-id="28543-111">예제의</span><span class="sxs-lookup"><span data-stu-id="28543-111">EXAMPLES</span></span>

### <span data-ttu-id="28543-112">예제 1: 컨테이너에서 보호 된 개체의 방향 수정</span><span class="sxs-lookup"><span data-stu-id="28543-112">Example 1: Modify the direction for a protected object in a container</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container  
PS C:\> Update-AzureSiteRecoveryProtectionDirection -Direction RecoveryToPrimary -ProtectionEntity $Protected 
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="28543-113">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 보호 된 컨테이너를 가져온 다음 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-113">The first command gets the protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="28543-114">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $Container에 저장 된 컨테이너에 속하는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28543-114">The second command gets the virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="28543-115">명령이 $Protected 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="28543-116">마지막 명령은 $Protected에 저장 된 개체에 대 한 방향을 RecoverToPrimary 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-116">The final command sets the direction to RecoverToPrimary for the objects stored in $Protected.</span></span>

## <span data-ttu-id="28543-117">변수</span><span class="sxs-lookup"><span data-stu-id="28543-117">PARAMETERS</span></span>

### <span data-ttu-id="28543-118">방향</span><span class="sxs-lookup"><span data-stu-id="28543-118">-Direction</span></span>
<span data-ttu-id="28543-119">커밋 방향을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-119">Specifies the direction of the commit.</span></span>
<span data-ttu-id="28543-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28543-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28543-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="28543-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="28543-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="28543-122">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="28543-123">-Profile</span></span>
<span data-ttu-id="28543-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28543-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="28543-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28543-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="28543-126">-ProtectionContainerId</span></span>
<span data-ttu-id="28543-127">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="28543-128">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에 속하는 보호 된 가상 컴퓨터의 방향을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-128">This cmdlet modifies the direction for a protected virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="28543-129">-ProtectionEntity</span></span>
<span data-ttu-id="28543-130">보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-130">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28543-131">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="28543-131">-ProtectionEntityId</span></span>
<span data-ttu-id="28543-132">보호 된 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-132">Specifies the ID of a protected virtual machine.</span></span>
<span data-ttu-id="28543-133">이 cmdlet은이 매개 변수에서 지정 하는 보호 된 가상 컴퓨터의 방향을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-133">This cmdlet modifies the direction for the protected virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="28543-134">-RecoveryPlan</span></span>
<span data-ttu-id="28543-135">복구 계획 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28543-136">-RPId</span><span class="sxs-lookup"><span data-stu-id="28543-136">-RPId</span></span>
<span data-ttu-id="28543-137">복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-137">Specifies the ID of a recovery plan.</span></span>
<span data-ttu-id="28543-138">이 cmdlet은이 매개 변수에서 지정 하는 복구 계획의 방향을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-138">This cmdlet modifies the direction for the recovery plan that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="28543-139">-WaitForCompletion</span></span>
<span data-ttu-id="28543-140">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="28543-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28543-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28543-141">CommonParameters</span></span>
<span data-ttu-id="28543-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28543-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28543-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28543-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28543-144">입력</span><span class="sxs-lookup"><span data-stu-id="28543-144">INPUTS</span></span>

## <span data-ttu-id="28543-145">출력</span><span class="sxs-lookup"><span data-stu-id="28543-145">OUTPUTS</span></span>

## <span data-ttu-id="28543-146">상속자</span><span class="sxs-lookup"><span data-stu-id="28543-146">NOTES</span></span>

## <span data-ttu-id="28543-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28543-147">RELATED LINKS</span></span>

[<span data-ttu-id="28543-148">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="28543-148">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="28543-149">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="28543-149">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


