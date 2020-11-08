---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 08A7556E-C07F-4B3B-B9D6-B241C72860FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b01ac318982b62499164cd54c9d9a51356ad9830
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047385"
---
# <span data-ttu-id="54d73-101">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-101">Set-WAPackVM</span></span>

## <span data-ttu-id="54d73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d73-102">SYNOPSIS</span></span>
<span data-ttu-id="54d73-103">가상 컴퓨터의 크기 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-103">Changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="54d73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54d73-104">SYNTAX</span></span>

```
Set-WAPackVM -VM <VirtualMachine> -VMSizeProfile <HardwareProfile> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="54d73-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54d73-105">DESCRIPTION</span></span>
<span data-ttu-id="54d73-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="54d73-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="54d73-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="54d73-109">**집합-WAPackVM** cmdlet이 가상 컴퓨터의 크기 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-109">The **Set-WAPackVM** cmdlet changes the size properties of a virtual machine.</span></span>

## <span data-ttu-id="54d73-110">예제의</span><span class="sxs-lookup"><span data-stu-id="54d73-110">EXAMPLES</span></span>

### <span data-ttu-id="54d73-111">예제 1: 가상 컴퓨터의 크기 지정</span><span class="sxs-lookup"><span data-stu-id="54d73-111">Example 1: Specify the size for a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-WAPackVM -Name "ContosoV126"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> Set-WAPackVM -VM $VirtualMachine -VMSizeProfile $SizeProfile
```

<span data-ttu-id="54d73-112">첫 번째 명령은 ContosoV126 **Apackvm** cmdlet을 사용 하 여 명명 된 가상 컴퓨터를 가져온 다음 해당 개체를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-112">The first command gets the virtual machine named ContosoV126 by using the **Get-WAPackVM** cmdlet, and then stores that object in the $VirtualMachine variable.</span></span>

<span data-ttu-id="54d73-113">두 번째 명령은 MediumSizeVM **Apackvmsizeprofile** cmdlet을 사용 하 여 명명 된 크기 프로필을 가져온 다음 해당 개체를 $SizeProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-113">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores that object in the $SizeProfile variable.</span></span>

<span data-ttu-id="54d73-114">마지막 명령은 $SizeProfile에 저장 된 크기 프로필을 $VirtualMachine에 저장 된 가상 컴퓨터에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-114">The final command assigns the size profile stored in $SizeProfile to the virtual machine stored in $VirtualMachine.</span></span>

## <span data-ttu-id="54d73-115">변수</span><span class="sxs-lookup"><span data-stu-id="54d73-115">PARAMETERS</span></span>

### <span data-ttu-id="54d73-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54d73-116">-PassThru</span></span>
<span data-ttu-id="54d73-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="54d73-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="54d73-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="54d73-119">-Profile</span></span>
<span data-ttu-id="54d73-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54d73-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54d73-122">-VM</span><span class="sxs-lookup"><span data-stu-id="54d73-122">-VM</span></span>
<span data-ttu-id="54d73-123">가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-123">Specifies a virtual machine.</span></span>
<span data-ttu-id="54d73-124">가상 컴퓨터를 가져오려면 **Get-WAPackVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-124">To obtain a virtual machine, use the **Get-WAPackVM** cmdlet.</span></span>

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

### <span data-ttu-id="54d73-125">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="54d73-125">-VMSizeProfile</span></span>
<span data-ttu-id="54d73-126">가상 머신의 크기 프로필을 **HardwareProfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-126">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="54d73-127">크기 프로필을 얻으려면 **Get-WAPackVMSizeProfile** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-127">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d73-128">CommonParameters</span></span>
<span data-ttu-id="54d73-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54d73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d73-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54d73-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d73-131">입력</span><span class="sxs-lookup"><span data-stu-id="54d73-131">INPUTS</span></span>

## <span data-ttu-id="54d73-132">출력</span><span class="sxs-lookup"><span data-stu-id="54d73-132">OUTPUTS</span></span>

## <span data-ttu-id="54d73-133">상속자</span><span class="sxs-lookup"><span data-stu-id="54d73-133">NOTES</span></span>

## <span data-ttu-id="54d73-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54d73-134">RELATED LINKS</span></span>

[<span data-ttu-id="54d73-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="54d73-136">새-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-136">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="54d73-137">제거-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-137">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="54d73-138">다시 시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-138">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="54d73-139">Resume-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-139">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="54d73-140">시작-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-140">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="54d73-141">중지-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-141">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="54d73-142">일시 중단-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="54d73-142">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="54d73-143">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="54d73-143">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)


