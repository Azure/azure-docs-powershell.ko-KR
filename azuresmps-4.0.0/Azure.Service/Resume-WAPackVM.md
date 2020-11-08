---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5E85F58B-7C70-4F4A-B218-08F9AF512B76
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8aba9c72e3911f59db88e9be4262ee90ea460a5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047395"
---
# <span data-ttu-id="9ff69-101">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-101">Resume-WAPackVM</span></span>

## <span data-ttu-id="9ff69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ff69-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff69-103">일시 중지 된 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-103">Resumes paused virtual machines.</span></span>

## <span data-ttu-id="9ff69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ff69-104">SYNTAX</span></span>

```
Resume-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ff69-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ff69-105">DESCRIPTION</span></span>
<span data-ttu-id="9ff69-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9ff69-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9ff69-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9ff69-109">**다시 시작-WAPackVM** cmdlet이 일시 중지 된 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-109">The **Resume-WAPackVM** cmdlet resumes paused virtual machines.</span></span>

## <span data-ttu-id="9ff69-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9ff69-110">EXAMPLES</span></span>

### <span data-ttu-id="9ff69-111">예제 1: 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="9ff69-111">Example 1: Resume a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Resume-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="9ff69-112">첫 번째 명령은 ContosoV126 **Apackvm** cmdlet을 사용 하 여 명명 된 가상 컴퓨터를 가져온 다음 해당 개체를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="9ff69-113">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-113">The second command resumes the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="9ff69-114">변수</span><span class="sxs-lookup"><span data-stu-id="9ff69-114">PARAMETERS</span></span>

### <span data-ttu-id="9ff69-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ff69-115">-PassThru</span></span>
<span data-ttu-id="9ff69-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9ff69-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ff69-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="9ff69-118">-Profile</span></span>
<span data-ttu-id="9ff69-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ff69-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ff69-121">-VM</span><span class="sxs-lookup"><span data-stu-id="9ff69-121">-VM</span></span>
<span data-ttu-id="9ff69-122">가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="9ff69-123">가상 컴퓨터를 가져오려면 **Get-WAPackVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="9ff69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff69-124">CommonParameters</span></span>
<span data-ttu-id="9ff69-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ff69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff69-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff69-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff69-127">입력</span><span class="sxs-lookup"><span data-stu-id="9ff69-127">INPUTS</span></span>

## <span data-ttu-id="9ff69-128">출력</span><span class="sxs-lookup"><span data-stu-id="9ff69-128">OUTPUTS</span></span>

## <span data-ttu-id="9ff69-129">상속자</span><span class="sxs-lookup"><span data-stu-id="9ff69-129">NOTES</span></span>

## <span data-ttu-id="9ff69-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ff69-130">RELATED LINKS</span></span>

[<span data-ttu-id="9ff69-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="9ff69-132">새-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="9ff69-133">제거-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="9ff69-134">다시 시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="9ff69-135">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-135">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="9ff69-136">시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-136">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="9ff69-137">중지-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="9ff69-138">일시 중단-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="9ff69-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


