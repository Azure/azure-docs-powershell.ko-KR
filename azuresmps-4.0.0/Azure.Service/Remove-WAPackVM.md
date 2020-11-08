---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D04D79CE-F183-4A8D-B925-F640D89377BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d7c4e6bd9365ccf45b730024b5841e4356f556a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047408"
---
# <span data-ttu-id="7f187-101">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-101">Remove-WAPackVM</span></span>

## <span data-ttu-id="7f187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f187-102">SYNOPSIS</span></span>
<span data-ttu-id="7f187-103">가상 컴퓨터 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-103">Removes virtual machine objects.</span></span>

## <span data-ttu-id="7f187-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f187-104">SYNTAX</span></span>

```
Remove-WAPackVM -VM <VirtualMachine> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f187-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f187-105">DESCRIPTION</span></span>
<span data-ttu-id="7f187-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7f187-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7f187-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7f187-109">**제거-WAPackVM** cmdlet은 가상 컴퓨터 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-109">The **Remove-WAPackVM** cmdlet removes virtual machine objects.</span></span>

## <span data-ttu-id="7f187-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7f187-110">EXAMPLES</span></span>

### <span data-ttu-id="7f187-111">예제 1: 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="7f187-111">Example 1: Remove a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="7f187-112">첫 번째 명령은 ContosoV126 **Apackvm** cmdlet을 사용 하 여 명명 된 가상 컴퓨터를 가져온 다음 해당 개체를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7f187-113">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-113">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7f187-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7f187-115">예제 2: 확인 하지 않고 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="7f187-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Remove-WAPackVM -VM $VirtualMachine -Force
```

<span data-ttu-id="7f187-116">첫 번째 명령은 ContosoV126 **Apackvm** cmdlet을 사용 하 여 명명 된 가상 컴퓨터를 가져온 다음 해당 개체를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-116">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7f187-117">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-117">The second command removes the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7f187-118">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="7f187-119">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f187-120">변수</span><span class="sxs-lookup"><span data-stu-id="7f187-120">PARAMETERS</span></span>

### <span data-ttu-id="7f187-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7f187-121">-Force</span></span>
<span data-ttu-id="7f187-122">Cmdlet에서 확인 메시지 없이 가상 컴퓨터를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-122">Indicates that the cmdlet removes a virtual machine without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7f187-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f187-123">-PassThru</span></span>
<span data-ttu-id="7f187-124">Cmdlet이 부울 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-124">Indicates that the cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="7f187-125">작업이 성공 하면 cmdlet은 $True 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-125">If the operation succeeds, the cmdlet returns a value of $True.</span></span>
<span data-ttu-id="7f187-126">그렇지 않으면 $False 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-126">Otherwise, it returns a value of $False.</span></span>
<span data-ttu-id="7f187-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f187-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="7f187-128">-Profile</span></span>
<span data-ttu-id="7f187-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f187-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f187-131">-VM</span><span class="sxs-lookup"><span data-stu-id="7f187-131">-VM</span></span>
<span data-ttu-id="7f187-132">가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-132">Specifies a virtual machine.</span></span>
<span data-ttu-id="7f187-133">가상 컴퓨터를 가져오려면 **Get-WAPackVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-133">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

```yaml
Type: VirtualMachine
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f187-134">-확인</span><span class="sxs-lookup"><span data-stu-id="7f187-134">-Confirm</span></span>
<span data-ttu-id="7f187-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f187-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f187-136">-WhatIf</span></span>
<span data-ttu-id="7f187-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f187-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f187-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f187-139">CommonParameters</span></span>
<span data-ttu-id="7f187-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f187-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f187-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f187-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f187-142">입력</span><span class="sxs-lookup"><span data-stu-id="7f187-142">INPUTS</span></span>

## <span data-ttu-id="7f187-143">출력</span><span class="sxs-lookup"><span data-stu-id="7f187-143">OUTPUTS</span></span>

## <span data-ttu-id="7f187-144">상속자</span><span class="sxs-lookup"><span data-stu-id="7f187-144">NOTES</span></span>

## <span data-ttu-id="7f187-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f187-145">RELATED LINKS</span></span>

[<span data-ttu-id="7f187-146">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-146">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="7f187-147">새-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-147">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="7f187-148">다시 시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-148">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="7f187-149">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-149">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="7f187-150">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-150">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="7f187-151">시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-151">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="7f187-152">중지-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-152">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="7f187-153">일시 중단-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="7f187-153">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


