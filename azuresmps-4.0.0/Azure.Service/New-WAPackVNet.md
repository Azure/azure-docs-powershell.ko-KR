---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047397"
---
# <span data-ttu-id="32fc8-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="32fc8-101">New-WAPackVNet</span></span>

## <span data-ttu-id="32fc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="32fc8-103">가상 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="32fc8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32fc8-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="32fc8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="32fc8-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="32fc8-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="32fc8-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="32fc8-109">**새-WAPackVNet** cmdlet은 가상화 된 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="32fc8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="32fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="32fc8-111">예제 1: 가상화 된 네트워크 만들기</span><span class="sxs-lookup"><span data-stu-id="32fc8-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="32fc8-112">첫 번째 명령은 먼저 가상화 된 새 네트워크를 추가 하려는 논리 네트워크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="32fc8-113">이 논리 네트워크 이름은 ContosoLogicalNetwork01입니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="32fc8-114">두 번째 및 마지막 명령은 이전에 검색 된 논리 네트워크, 이름 (ContosoVNett01) 및 설명 (설명)을 사용 하 여 가상화 된 네트워크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="32fc8-115">변수</span><span class="sxs-lookup"><span data-stu-id="32fc8-115">PARAMETERS</span></span>

### <span data-ttu-id="32fc8-116">-설명</span><span class="sxs-lookup"><span data-stu-id="32fc8-116">-Description</span></span>
<span data-ttu-id="32fc8-117">가상화 된 네트워크에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-117">Specifies a description for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fc8-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="32fc8-118">-LogicalNetwork</span></span>
<span data-ttu-id="32fc8-119">가상화 된 네트워크와 연결 된 LogicalNetwork를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32fc8-120">-이름</span><span class="sxs-lookup"><span data-stu-id="32fc8-120">-Name</span></span>
<span data-ttu-id="32fc8-121">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-121">Specifies a name for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fc8-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="32fc8-122">-Profile</span></span>
<span data-ttu-id="32fc8-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32fc8-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32fc8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fc8-125">CommonParameters</span></span>
<span data-ttu-id="32fc8-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32fc8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fc8-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32fc8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fc8-128">입력</span><span class="sxs-lookup"><span data-stu-id="32fc8-128">INPUTS</span></span>

## <span data-ttu-id="32fc8-129">출력</span><span class="sxs-lookup"><span data-stu-id="32fc8-129">OUTPUTS</span></span>

## <span data-ttu-id="32fc8-130">상속자</span><span class="sxs-lookup"><span data-stu-id="32fc8-130">NOTES</span></span>

## <span data-ttu-id="32fc8-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32fc8-131">RELATED LINKS</span></span>

[<span data-ttu-id="32fc8-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="32fc8-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="32fc8-133">제거-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="32fc8-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


