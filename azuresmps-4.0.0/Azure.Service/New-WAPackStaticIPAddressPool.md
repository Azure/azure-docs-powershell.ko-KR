---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047381"
---
# <span data-ttu-id="e2ce0-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2ce0-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="e2ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ce0-103">고정 IP 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="e2ce0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2ce0-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2ce0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ce0-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e2ce0-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e2ce0-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e2ce0-109">**새 WAPackStaticIPAddressPool** cmdlet은 고정 IP 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="e2ce0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e2ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="e2ce0-111">예제 1: 고정 IP 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="e2ce0-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="e2ce0-112">첫 번째 명령은 먼저 정적 IP 주소 풀을 추가 하려는 가상 컴퓨터 네트워크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="e2ce0-113">이 가상 컴퓨터 네트워크의 이름은 ContosoVNet01입니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="e2ce0-114">두 번째 명령은 이전에 검색 된 가상 컴퓨터 네트워크를 사용 하 여 고정 IP 주소 풀을 추가 하려는 ContosoVMSubnet01 이라는 가상 컴퓨터 서브넷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="e2ce0-115">마지막 명령은 이름 ContosoStaticIpAddressPool01과 범위 시작 192.168.1.0, 그리고 범위 end 192.168.1.10를 사용 하 여 새 고정 IP 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="e2ce0-116">변수</span><span class="sxs-lookup"><span data-stu-id="e2ce0-116">PARAMETERS</span></span>

### <span data-ttu-id="e2ce0-117">-Ipaddressa End</span><span class="sxs-lookup"><span data-stu-id="e2ce0-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="e2ce0-118">고정 IP 주소 풀에 대 한 IP 주소 범위 종료를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-118">Specifies an IP address range end for the static IP address pool.</span></span>

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

### <span data-ttu-id="e2ce0-119">-Ipaddressip 시작</span><span class="sxs-lookup"><span data-stu-id="e2ce0-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="e2ce0-120">고정 IP 주소 풀에 대 한 IP 주소 범위 시작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-120">Specifies an IP address range start for the static IP address pool.</span></span>

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

### <span data-ttu-id="e2ce0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e2ce0-121">-Name</span></span>
<span data-ttu-id="e2ce0-122">고정 IP 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-122">Specifies a name for the static IP address pool.</span></span>

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

### <span data-ttu-id="e2ce0-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="e2ce0-123">-Profile</span></span>
<span data-ttu-id="e2ce0-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2ce0-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2ce0-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="e2ce0-126">-VMSubnet</span></span>
<span data-ttu-id="e2ce0-127">고정 IP 주소 풀과 연결 된 VMSubnet을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

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

### <span data-ttu-id="e2ce0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ce0-128">CommonParameters</span></span>
<span data-ttu-id="e2ce0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2ce0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ce0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ce0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ce0-131">입력</span><span class="sxs-lookup"><span data-stu-id="e2ce0-131">INPUTS</span></span>

## <span data-ttu-id="e2ce0-132">출력</span><span class="sxs-lookup"><span data-stu-id="e2ce0-132">OUTPUTS</span></span>

## <span data-ttu-id="e2ce0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e2ce0-133">NOTES</span></span>

## <span data-ttu-id="e2ce0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2ce0-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2ce0-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2ce0-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="e2ce0-136">제거-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2ce0-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


