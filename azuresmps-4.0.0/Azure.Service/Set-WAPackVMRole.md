---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047383"
---
# <span data-ttu-id="9af2e-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9af2e-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="9af2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af2e-102">SYNOPSIS</span></span>
<span data-ttu-id="9af2e-103">가상 컴퓨터 역할의 인스턴스 수 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="9af2e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9af2e-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9af2e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9af2e-105">DESCRIPTION</span></span>
<span data-ttu-id="9af2e-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="9af2e-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9af2e-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9af2e-109">**WAPackVMRole** cmdlet은 가상 컴퓨터 역할의 인스턴스 수 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="9af2e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9af2e-110">EXAMPLES</span></span>

### <span data-ttu-id="9af2e-111">예제 1: 가상 컴퓨터 역할의 인스턴스 수 지정</span><span class="sxs-lookup"><span data-stu-id="9af2e-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="9af2e-112">첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole01 이라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="9af2e-113">두 번째 및 마지막 명령은 $VMRole에 저장 된 가상 컴퓨터 역할의 새 인스턴스 수를 3으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="9af2e-114">변수</span><span class="sxs-lookup"><span data-stu-id="9af2e-114">PARAMETERS</span></span>

### <span data-ttu-id="9af2e-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="9af2e-115">-InstanceCount</span></span>
<span data-ttu-id="9af2e-116">가상 컴퓨터 역할의 인스턴스 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af2e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9af2e-117">-PassThru</span></span>
<span data-ttu-id="9af2e-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9af2e-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9af2e-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="9af2e-120">-Profile</span></span>
<span data-ttu-id="9af2e-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9af2e-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9af2e-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="9af2e-123">-VMRole</span></span>
<span data-ttu-id="9af2e-124">가상 컴퓨터 역할을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="9af2e-125">가상 컴퓨터 역할을 얻으려면 **Get-WAPackVMRole** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9af2e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af2e-126">CommonParameters</span></span>
<span data-ttu-id="9af2e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9af2e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af2e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af2e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af2e-129">입력</span><span class="sxs-lookup"><span data-stu-id="9af2e-129">INPUTS</span></span>

## <span data-ttu-id="9af2e-130">출력</span><span class="sxs-lookup"><span data-stu-id="9af2e-130">OUTPUTS</span></span>

## <span data-ttu-id="9af2e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="9af2e-131">NOTES</span></span>

## <span data-ttu-id="9af2e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9af2e-132">RELATED LINKS</span></span>

[<span data-ttu-id="9af2e-133">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9af2e-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="9af2e-134">새로운 WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9af2e-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="9af2e-135">제거-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="9af2e-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


