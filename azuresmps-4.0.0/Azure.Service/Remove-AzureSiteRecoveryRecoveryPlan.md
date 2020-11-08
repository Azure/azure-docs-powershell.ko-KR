---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046111"
---
# <span data-ttu-id="af586-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af586-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="af586-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af586-102">SYNOPSIS</span></span>
<span data-ttu-id="af586-103">사이트 복구에서 사이트 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="af586-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af586-104">SYNTAX</span></span>

### <span data-ttu-id="af586-105">ByRPObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="af586-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af586-106">ById</span><span class="sxs-lookup"><span data-stu-id="af586-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af586-107">설명은</span><span class="sxs-lookup"><span data-stu-id="af586-107">DESCRIPTION</span></span>
<span data-ttu-id="af586-108">**AzureSiteRecoveryRecoveryPlan** cmdlet은 현재 Azure site recovery에서 사이트 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="af586-109">예제의</span><span class="sxs-lookup"><span data-stu-id="af586-109">EXAMPLES</span></span>

### <span data-ttu-id="af586-110">예제 1: 복구 계획 제거</span><span class="sxs-lookup"><span data-stu-id="af586-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="af586-111">첫 번째 명령은 **AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 하 여 사이트 복구 계획을 얻은 다음 $RecoveryPlan 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="af586-112">두 번째 명령은 $RecoveryPlan 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="af586-113">변수</span><span class="sxs-lookup"><span data-stu-id="af586-113">PARAMETERS</span></span>

### <span data-ttu-id="af586-114">-Force</span><span class="sxs-lookup"><span data-stu-id="af586-114">-Force</span></span>
<span data-ttu-id="af586-115">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af586-116">-Id</span><span class="sxs-lookup"><span data-stu-id="af586-116">-Id</span></span>
<span data-ttu-id="af586-117">제거할 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af586-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="af586-118">-Profile</span></span>
<span data-ttu-id="af586-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af586-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="af586-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af586-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af586-121">-RecoveryPlan</span></span>
<span data-ttu-id="af586-122">제거할 복구 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-122">Specifies the recovery plan to remove.</span></span>

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

### <span data-ttu-id="af586-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="af586-123">-WaitForCompletion</span></span>
<span data-ttu-id="af586-124">Cmdlet이 Windows PowerShell 콘솔에 제어를 반환 하기 전에 작업이 완료 될 때까지 대기 하 고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af586-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="af586-125">-확인</span><span class="sxs-lookup"><span data-stu-id="af586-125">-Confirm</span></span>
<span data-ttu-id="af586-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af586-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af586-127">-WhatIf</span></span>
<span data-ttu-id="af586-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af586-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af586-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af586-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af586-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af586-130">CommonParameters</span></span>
<span data-ttu-id="af586-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af586-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af586-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af586-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af586-133">입력</span><span class="sxs-lookup"><span data-stu-id="af586-133">INPUTS</span></span>

## <span data-ttu-id="af586-134">출력</span><span class="sxs-lookup"><span data-stu-id="af586-134">OUTPUTS</span></span>

## <span data-ttu-id="af586-135">상속자</span><span class="sxs-lookup"><span data-stu-id="af586-135">NOTES</span></span>

## <span data-ttu-id="af586-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af586-136">RELATED LINKS</span></span>

[<span data-ttu-id="af586-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af586-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="af586-138">새로운 AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af586-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="af586-139">업데이트-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="af586-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


