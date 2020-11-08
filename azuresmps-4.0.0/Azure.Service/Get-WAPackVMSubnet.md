---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0E358CEF-69E4-4639-918C-CE593E97B189
online version: ''
schema: 2.0.0
ms.openlocfilehash: d534a1734a49739db648558e8d7e62b22e43d561
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047355"
---
# <span data-ttu-id="d9569-101">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="d9569-101">Get-WAPackVMSubnet</span></span>

## <span data-ttu-id="d9569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9569-102">SYNOPSIS</span></span>
<span data-ttu-id="d9569-103">가상 컴퓨터 서브넷 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-103">Gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="d9569-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9569-104">SYNTAX</span></span>

### <span data-ttu-id="d9569-105">FromVMNetworkObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9569-105">FromVMNetworkObject (Default)</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9569-106">FromName</span><span class="sxs-lookup"><span data-stu-id="d9569-106">FromName</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9569-107">찡그린 Mid</span><span class="sxs-lookup"><span data-stu-id="d9569-107">FromId</span></span>
```
Get-WAPackVMSubnet -VNet <VMNetwork> -ID <Guid> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9569-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d9569-108">DESCRIPTION</span></span>
<span data-ttu-id="d9569-109">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d9569-110">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d9569-111">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d9569-112">**Get-WAPackVMSubnet** cmdlet은 가상 컴퓨터 서브넷 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-112">The **Get-WAPackVMSubnet** cmdlet gets virtual machine subnet objects.</span></span>

## <span data-ttu-id="d9569-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d9569-113">EXAMPLES</span></span>

### <span data-ttu-id="d9569-114">예제 1: 이름을 사용 하 여 가상 컴퓨터 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9569-114">Example 1: Get a virtual machine subnet by using a name</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMTemplate -VNet $VNet -Name "ContosoSubnet01"
```

<span data-ttu-id="d9569-115">이 명령은 ContosoSubnet01 이라는 가상 컴퓨터 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-115">This command gets the virtual machine subnet named ContosoSubnet01.</span></span>

### <span data-ttu-id="d9569-116">예제 2: ID를 사용 하 여 가상 컴퓨터 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9569-116">Example 2: Get a virtual machine subnet by using an ID</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="d9569-117">이 명령은 지정 된 ID를 가진 가상 컴퓨터 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-117">This command gets the virtual machine subnet that has the specified ID.</span></span>

### <span data-ttu-id="d9569-118">예제 3: 주어진 가상화 된 네트워크에서 모든 가상 컴퓨터 서브넷 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9569-118">Example 3: Get all virtual machine subnets from a given virtualized network</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Get-WAPackVMSubnet -VNet $VNet
```

<span data-ttu-id="d9569-119">이 명령은 주어진 가상화 네트워크에서 모든 가상 머신 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-119">This command gets all the virtual machine subnets from a given virtualized network.</span></span>

## <span data-ttu-id="d9569-120">변수</span><span class="sxs-lookup"><span data-stu-id="d9569-120">PARAMETERS</span></span>

### <span data-ttu-id="d9569-121">-ID</span><span class="sxs-lookup"><span data-stu-id="d9569-121">-ID</span></span>
<span data-ttu-id="d9569-122">가상 컴퓨터 서브넷의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-122">Specifies the unique ID of a virtual machine subnet.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9569-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d9569-123">-Name</span></span>
<span data-ttu-id="d9569-124">가상 컴퓨터 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-124">Specifies the name of a virtual machine subnet.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9569-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="d9569-125">-Profile</span></span>
<span data-ttu-id="d9569-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9569-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9569-128">-VNet</span><span class="sxs-lookup"><span data-stu-id="d9569-128">-VNet</span></span>
<span data-ttu-id="d9569-129">가상 머신 서브넷과 연결 된 VNet을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-129">Specifies the VNet associated with a virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9569-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9569-130">CommonParameters</span></span>
<span data-ttu-id="d9569-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9569-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9569-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9569-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9569-133">입력</span><span class="sxs-lookup"><span data-stu-id="d9569-133">INPUTS</span></span>

## <span data-ttu-id="d9569-134">출력</span><span class="sxs-lookup"><span data-stu-id="d9569-134">OUTPUTS</span></span>

## <span data-ttu-id="d9569-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d9569-135">NOTES</span></span>

## <span data-ttu-id="d9569-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9569-136">RELATED LINKS</span></span>

[<span data-ttu-id="d9569-137">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="d9569-137">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="d9569-138">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="d9569-138">New-WAPackVMSubnet</span></span>](./New-WAPackVMSubnet.md)

[<span data-ttu-id="d9569-139">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="d9569-139">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


