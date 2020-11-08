---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 1415BBA3-3F55-46A9-B20B-DFA72342BDF4
online version: ''
schema: 2.0.0
ms.openlocfilehash: ec7883b996e5da367884fd7d051a5299c6d62a9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046423"
---
# <span data-ttu-id="0aa85-101">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0aa85-101">Set-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="0aa85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aa85-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa85-103">사이트 복구 보호 엔터티의 상태를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-103">Sets the state for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="0aa85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0aa85-104">SYNTAX</span></span>

### <span data-ttu-id="0aa85-105">ByPEObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="0aa85-105">ByPEObject (Default)</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aa85-106">ByIDs</span><span class="sxs-lookup"><span data-stu-id="0aa85-106">ByIDs</span></span>
```
Set-AzureSiteRecoveryProtectionEntity -Id <String> -ProtectionContainerId <String>
 [-ProtectionProfile <ASRProtectionProfile>] -Protection <String> [-OSDiskName <String>] [-OS <String>]
 [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aa85-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0aa85-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa85-108">**AzureSiteRecoveryProtectionEntity** Cmdlet은 Azure Site Recovery 보호 엔터티의 보호를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-108">The **Set-AzureSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="0aa85-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0aa85-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa85-110">예제 1: 컨테이너에서 개체에 대 한 보호 사용</span><span class="sxs-lookup"><span data-stu-id="0aa85-110">Example 1: Enable protection for objects in a container</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer -Name "Cloud17"
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer -Name "VM01"
PS C:\> Set-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ ProtectionEntity -Protection Enable -ProtectionProfile $ProtectionContainer.AvailableProtectionProfiles[0] -OS Windows
```

<span data-ttu-id="0aa85-111">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 현재 Azure 사이트 자격 증명 모음에 대 한 컨테이너를 가져온 다음 $ProtectionContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-111">The first command gets containers for the current Azure Site vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="0aa85-112">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $ProtectionContainer에 저장 된 컨테이너에 속하는 보호 된 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-112">The second command gets the protected virtual machines that belong to the container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="0aa85-113">명령이 $ProtectionEntity 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-113">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="0aa85-114">마지막 명령은 $ProtectionEntity에 저장 된 엔터티에 대해 보호를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-114">The final command enables protection for the entities stored in $ProtectionEntity.</span></span>

## <span data-ttu-id="0aa85-115">변수</span><span class="sxs-lookup"><span data-stu-id="0aa85-115">PARAMETERS</span></span>

### <span data-ttu-id="0aa85-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0aa85-116">-Force</span></span>
<span data-ttu-id="0aa85-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0aa85-118">-Id</span><span class="sxs-lookup"><span data-stu-id="0aa85-118">-Id</span></span>
<span data-ttu-id="0aa85-119">보호를 사용 하거나 사용 하지 않도록 설정할 보호 된 가상 컴퓨터의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-119">Specifies the ID of a protected virtual machine for which to enable or disable protection.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-120">-OS</span><span class="sxs-lookup"><span data-stu-id="0aa85-120">-OS</span></span>
<span data-ttu-id="0aa85-121">운영 체제 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-121">Specifies the operating system type.</span></span>
<span data-ttu-id="0aa85-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0aa85-123">창을</span><span class="sxs-lookup"><span data-stu-id="0aa85-123">Windows</span></span>
- <span data-ttu-id="0aa85-124">Linux</span><span class="sxs-lookup"><span data-stu-id="0aa85-124">Linux</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-125">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="0aa85-125">-OSDiskName</span></span>
<span data-ttu-id="0aa85-126">운영 체제를 포함 하는 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-126">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="0aa85-127">-Profile</span></span>
<span data-ttu-id="0aa85-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0aa85-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0aa85-130">-보호</span><span class="sxs-lookup"><span data-stu-id="0aa85-130">-Protection</span></span>
<span data-ttu-id="0aa85-131">보호를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-131">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="0aa85-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0aa85-133">설정할</span><span class="sxs-lookup"><span data-stu-id="0aa85-133">Enable</span></span>
- <span data-ttu-id="0aa85-134">설정할</span><span class="sxs-lookup"><span data-stu-id="0aa85-134">Disable</span></span>

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

### <span data-ttu-id="0aa85-135">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="0aa85-135">-ProtectionContainerId</span></span>
<span data-ttu-id="0aa85-136">보호 된 컨테이너의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-136">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="0aa85-137">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에 속하는 가상 컴퓨터에 대 한 보호를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-137">This cmdlet enables or disables protection for a virtual machine that belongs to the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByIDs
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-138">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0aa85-138">-ProtectionEntity</span></span>
<span data-ttu-id="0aa85-139">보호 엔터티 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-139">Specifies the protection entity object.</span></span>

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

### <span data-ttu-id="0aa85-140">-ProtectionProfile</span><span class="sxs-lookup"><span data-stu-id="0aa85-140">-ProtectionProfile</span></span>
<span data-ttu-id="0aa85-141">보호를 사용 하도록 설정 하는 보호 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-141">Specifies a protection profile to enable protection.</span></span>
<span data-ttu-id="0aa85-142">연결 된 보호 컨테이너에서 사용 가능한 보호 프로필 중 하나인 **ASRProtectionProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-142">Specify an **ASRProtectionProfile** object that is one of the available protection profiles in the associated protection container.</span></span>

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-143">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0aa85-143">-WaitForCompletion</span></span>
<span data-ttu-id="0aa85-144">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-144">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="0aa85-145">-확인</span><span class="sxs-lookup"><span data-stu-id="0aa85-145">-Confirm</span></span>
<span data-ttu-id="0aa85-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aa85-147">-WhatIf</span></span>
<span data-ttu-id="0aa85-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aa85-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0aa85-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa85-150">CommonParameters</span></span>
<span data-ttu-id="0aa85-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0aa85-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa85-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa85-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa85-153">입력</span><span class="sxs-lookup"><span data-stu-id="0aa85-153">INPUTS</span></span>

## <span data-ttu-id="0aa85-154">출력</span><span class="sxs-lookup"><span data-stu-id="0aa85-154">OUTPUTS</span></span>

## <span data-ttu-id="0aa85-155">상속자</span><span class="sxs-lookup"><span data-stu-id="0aa85-155">NOTES</span></span>

## <span data-ttu-id="0aa85-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0aa85-156">RELATED LINKS</span></span>

[<span data-ttu-id="0aa85-157">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0aa85-157">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="0aa85-158">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0aa85-158">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="0aa85-159">업데이트-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0aa85-159">Update-AzureSiteRecoveryProtectionEntity</span></span>](./Update-AzureSiteRecoveryProtectionEntity.md)


