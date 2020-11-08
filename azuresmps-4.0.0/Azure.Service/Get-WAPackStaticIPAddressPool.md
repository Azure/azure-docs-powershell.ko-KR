---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047431"
---
# <span data-ttu-id="35580-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="35580-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="35580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35580-102">SYNOPSIS</span></span>
<span data-ttu-id="35580-103">고정 IP 주소 풀 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35580-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="35580-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35580-104">SYNTAX</span></span>

### <span data-ttu-id="35580-105">FromVMSubnetObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="35580-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="35580-106">FromName</span><span class="sxs-lookup"><span data-stu-id="35580-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="35580-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35580-107">DESCRIPTION</span></span>
<span data-ttu-id="35580-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="35580-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="35580-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="35580-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="35580-111">**Get-WAPackStaticIPAddressPool** cmdlet은 고정 IP 주소 풀 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35580-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="35580-112">예제의</span><span class="sxs-lookup"><span data-stu-id="35580-112">EXAMPLES</span></span>

### <span data-ttu-id="35580-113">예제 1: 지정 된 VMSubnet에서 고정 IP 주소 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="35580-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="35580-114">이 명령은 지정 된 VMSubnet에서 ContosoStaticIPAddressPool01 이라는 고정 IP 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35580-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="35580-115">예제 2: 지정 된 VMSubnet에서 모든 고정 IP 주소 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="35580-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="35580-116">이 명령은 지정 된 VMSubet 모든 고정 IP 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35580-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="35580-117">변수</span><span class="sxs-lookup"><span data-stu-id="35580-117">PARAMETERS</span></span>

### <span data-ttu-id="35580-118">-이름</span><span class="sxs-lookup"><span data-stu-id="35580-118">-Name</span></span>
<span data-ttu-id="35580-119">고정 IP 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-119">Specifies the name of a static IP address pool.</span></span>

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

### <span data-ttu-id="35580-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="35580-120">-Profile</span></span>
<span data-ttu-id="35580-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="35580-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="35580-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="35580-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="35580-123">-VMSubnet</span></span>
<span data-ttu-id="35580-124">고정 IP 주소 풀에 연결 된 **VMSubnet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="35580-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35580-125">CommonParameters</span></span>
<span data-ttu-id="35580-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35580-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35580-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35580-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35580-128">입력</span><span class="sxs-lookup"><span data-stu-id="35580-128">INPUTS</span></span>

## <span data-ttu-id="35580-129">출력</span><span class="sxs-lookup"><span data-stu-id="35580-129">OUTPUTS</span></span>

## <span data-ttu-id="35580-130">상속자</span><span class="sxs-lookup"><span data-stu-id="35580-130">NOTES</span></span>

## <span data-ttu-id="35580-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35580-131">RELATED LINKS</span></span>

[<span data-ttu-id="35580-132">새로운 WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="35580-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="35580-133">제거-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="35580-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


