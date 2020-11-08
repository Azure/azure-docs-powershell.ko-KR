---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045886"
---
# <span data-ttu-id="5163d-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5163d-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="5163d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5163d-102">SYNOPSIS</span></span>
<span data-ttu-id="5163d-103">가상 컴퓨터 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="5163d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5163d-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5163d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5163d-105">DESCRIPTION</span></span>
<span data-ttu-id="5163d-106">**새-WAPackVMSubnet** cmdlet은 가상 컴퓨터 서브넷을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="5163d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5163d-107">EXAMPLES</span></span>

### <span data-ttu-id="5163d-108">예제 1: 가상 컴퓨터 서브넷 만들기</span><span class="sxs-lookup"><span data-stu-id="5163d-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="5163d-109">첫 번째 명령은 새 가상 컴퓨터 서브넷을 추가 하려는 가상 컴퓨터 네트워크를 먼저 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="5163d-110">이 가상 컴퓨터 네트워크의 이름은 ContosoVNet01입니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="5163d-111">두 번째 명령은 이전에 가상 머신 네트워크를 사용 하 여 가상 머신 서브넷을 만들고 이름 ContosoVMSubnet01와 서브넷 192.168.1.0/24를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="5163d-112">변수</span><span class="sxs-lookup"><span data-stu-id="5163d-112">PARAMETERS</span></span>

### <span data-ttu-id="5163d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5163d-113">-Name</span></span>
<span data-ttu-id="5163d-114">가상 컴퓨터 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="5163d-115">-프로필</span><span class="sxs-lookup"><span data-stu-id="5163d-115">-Profile</span></span>
<span data-ttu-id="5163d-116">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5163d-117">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5163d-118">-서브넷</span><span class="sxs-lookup"><span data-stu-id="5163d-118">-Subnet</span></span>
<span data-ttu-id="5163d-119">가상 컴퓨터 서브넷에 대 한 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="5163d-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="5163d-120">-VNet</span></span>
<span data-ttu-id="5163d-121">가상 머신 서브넷과 연결 된 VNet을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

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

### <span data-ttu-id="5163d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5163d-122">CommonParameters</span></span>
<span data-ttu-id="5163d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5163d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5163d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5163d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5163d-125">입력</span><span class="sxs-lookup"><span data-stu-id="5163d-125">INPUTS</span></span>

## <span data-ttu-id="5163d-126">출력</span><span class="sxs-lookup"><span data-stu-id="5163d-126">OUTPUTS</span></span>

## <span data-ttu-id="5163d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="5163d-127">NOTES</span></span>

## <span data-ttu-id="5163d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5163d-128">RELATED LINKS</span></span>

[<span data-ttu-id="5163d-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5163d-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="5163d-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="5163d-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="5163d-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="5163d-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


