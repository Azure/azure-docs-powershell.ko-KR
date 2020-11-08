---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7766E3D-D8C2-42F1-840A-8EA633E98500
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8a85934deb617b4f0d8e85ee3162222f16dd294
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047407"
---
# <span data-ttu-id="893bd-101">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="893bd-101">Remove-WAPackVMSubnet</span></span>

## <span data-ttu-id="893bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="893bd-102">SYNOPSIS</span></span>
<span data-ttu-id="893bd-103">가상 컴퓨터 서브넷 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-103">Removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="893bd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="893bd-104">SYNTAX</span></span>

```
Remove-WAPackVMSubnet -VMSubnet <VMSubnet> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="893bd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="893bd-105">DESCRIPTION</span></span>
<span data-ttu-id="893bd-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="893bd-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="893bd-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="893bd-109">**Remove-WAPackVMSubnet** cmdlet은 가상 컴퓨터 서브넷 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-109">The **Remove-WAPackVMSubnet** cmdlet removes virtual machine subnet objects.</span></span>

## <span data-ttu-id="893bd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="893bd-110">EXAMPLES</span></span>

### <span data-ttu-id="893bd-111">예제 1: 가상 컴퓨터 서브넷 제거</span><span class="sxs-lookup"><span data-stu-id="893bd-111">Example 1: Remove a virtual machine subnet</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet01"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet
```

<span data-ttu-id="893bd-112">첫 번째 명령은 **Get-help Apackvmsubnet** cmdlet을 사용 하 여 ContosoVMSubnet01 이라는 가상 컴퓨터 서브넷을 가져온 다음 해당 개체를 $VMSubnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-112">The first command gets the virtual machine subnet named ContosoVMSubnet01 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="893bd-113">두 번째 명령은 $VMSubnet에 저장 된 가상 컴퓨터 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-113">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="893bd-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="893bd-115">예제 2: 확인 하지 않고 가상 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="893bd-115">Example 2: Remove a virtual machine without confirmation</span></span>
```
PS C:\> $VMSubnet = Get-WAPackVMSubnet -Name "ContosoVMSubnet02"
PS C:\> Remove-WAPackVMSubnet -VMSubnet $VMSubnet -Force
```

<span data-ttu-id="893bd-116">첫 번째 명령은 **Get-WAPackVMSubnet** cmdlet을 사용 하 여 ContosoVMSubnet02 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $VMSubnet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-116">The first command gets the cloud service named ContosoVMSubnet02 by using the **Get-WAPackVMSubnet** cmdlet, and then stores that object in the $VMSubnet variable.</span></span>

<span data-ttu-id="893bd-117">두 번째 명령은 $VMSubnet에 저장 된 가상 컴퓨터 서브넷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-117">The second command removes the virtual machine subnet stored in $VMSubnet.</span></span>
<span data-ttu-id="893bd-118">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="893bd-119">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="893bd-120">변수</span><span class="sxs-lookup"><span data-stu-id="893bd-120">PARAMETERS</span></span>

### <span data-ttu-id="893bd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="893bd-121">-Force</span></span>
<span data-ttu-id="893bd-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="893bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="893bd-123">-PassThru</span></span>
<span data-ttu-id="893bd-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="893bd-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="893bd-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="893bd-126">-Profile</span></span>
<span data-ttu-id="893bd-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="893bd-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="893bd-129">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="893bd-129">-VMSubnet</span></span>
<span data-ttu-id="893bd-130">가상 컴퓨터 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-130">Specifies a virtual machine subnet.</span></span>
<span data-ttu-id="893bd-131">가상 컴퓨터 서브넷을 얻으려면 **Get WAPackVMSubnet** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-131">To obtain a virtual machine subnet, use the **Get-WAPackVMSubnet** cmdlet.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="893bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893bd-132">CommonParameters</span></span>
<span data-ttu-id="893bd-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="893bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893bd-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893bd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893bd-135">입력</span><span class="sxs-lookup"><span data-stu-id="893bd-135">INPUTS</span></span>

## <span data-ttu-id="893bd-136">출력</span><span class="sxs-lookup"><span data-stu-id="893bd-136">OUTPUTS</span></span>

## <span data-ttu-id="893bd-137">상속자</span><span class="sxs-lookup"><span data-stu-id="893bd-137">NOTES</span></span>

## <span data-ttu-id="893bd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="893bd-138">RELATED LINKS</span></span>

[<span data-ttu-id="893bd-139">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="893bd-139">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="893bd-140">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="893bd-140">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)


