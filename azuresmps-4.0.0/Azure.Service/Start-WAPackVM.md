---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8A6B4C8C-B990-443B-9157-B5C35824269A
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2d87c92f18c3aeb25aad210922dea0c93287fa6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047424"
---
# <span data-ttu-id="40353-101">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-101">Start-WAPackVM</span></span>

## <span data-ttu-id="40353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40353-102">SYNOPSIS</span></span>
<span data-ttu-id="40353-103">가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-103">Starts a virtual machine.</span></span>

## <span data-ttu-id="40353-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40353-104">SYNTAX</span></span>

```
Start-WAPackVM -VM <VirtualMachine> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40353-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40353-105">DESCRIPTION</span></span>
<span data-ttu-id="40353-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="40353-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="40353-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="40353-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="40353-109">**시작-WAPackVM** cmdlet은 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-109">The **Start-WAPackVM** cmdlet starts a virtual machine.</span></span>

## <span data-ttu-id="40353-110">예제의</span><span class="sxs-lookup"><span data-stu-id="40353-110">EXAMPLES</span></span>

### <span data-ttu-id="40353-111">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="40353-111">Example 1: Start a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> Start-WAPackVM -VM $VirtualMachine
```

<span data-ttu-id="40353-112">첫 번째 명령은 ContosoV126 **Apackvm** cmdlet을 사용 하 여 명명 된 가상 컴퓨터를 가져온 다음 해당 개체를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="40353-113">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-113">The second command starts the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="40353-114">변수</span><span class="sxs-lookup"><span data-stu-id="40353-114">PARAMETERS</span></span>

### <span data-ttu-id="40353-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40353-115">-PassThru</span></span>
<span data-ttu-id="40353-116">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40353-117">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40353-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="40353-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="40353-118">-Profile</span></span>
<span data-ttu-id="40353-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40353-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="40353-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40353-121">-VM</span><span class="sxs-lookup"><span data-stu-id="40353-121">-VM</span></span>
<span data-ttu-id="40353-122">가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-122">Specifies a virtual machine.</span></span>
<span data-ttu-id="40353-123">가상 컴퓨터를 가져오려면 **Get-WAPackVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-123">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="40353-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40353-124">CommonParameters</span></span>
<span data-ttu-id="40353-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40353-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40353-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40353-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40353-127">입력</span><span class="sxs-lookup"><span data-stu-id="40353-127">INPUTS</span></span>

## <span data-ttu-id="40353-128">출력</span><span class="sxs-lookup"><span data-stu-id="40353-128">OUTPUTS</span></span>

## <span data-ttu-id="40353-129">상속자</span><span class="sxs-lookup"><span data-stu-id="40353-129">NOTES</span></span>

## <span data-ttu-id="40353-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40353-130">RELATED LINKS</span></span>

[<span data-ttu-id="40353-131">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-131">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="40353-132">새-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-132">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="40353-133">제거-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-133">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="40353-134">다시 시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-134">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="40353-135">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-135">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="40353-136">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-136">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="40353-137">중지-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-137">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="40353-138">일시 중단-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="40353-138">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)


