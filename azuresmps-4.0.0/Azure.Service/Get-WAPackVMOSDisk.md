---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047352"
---
# <span data-ttu-id="a1384-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="a1384-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="a1384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1384-102">SYNOPSIS</span></span>
<span data-ttu-id="a1384-103">가상 컴퓨터에 대 한 운영 체제 디스크 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="a1384-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1384-104">SYNTAX</span></span>

### <span data-ttu-id="a1384-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1384-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1384-106">찡그린 Mid</span><span class="sxs-lookup"><span data-stu-id="a1384-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a1384-107">FromName</span><span class="sxs-lookup"><span data-stu-id="a1384-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a1384-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1384-108">DESCRIPTION</span></span>
<span data-ttu-id="a1384-109">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="a1384-110">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a1384-111">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a1384-112">**WAPackVMOSDisk** cmdlet은 가상 컴퓨터의 운영 체제 디스크 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="a1384-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a1384-113">EXAMPLES</span></span>

### <span data-ttu-id="a1384-114">예제 1: 이름을 사용 하 여 운영 체제 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1384-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="a1384-115">이 명령은 ContosoOSDisk 이라는 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="a1384-116">예제 2: ID를 사용 하 여 운영 체제 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1384-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="a1384-117">이 명령은 지정 된 ID의 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="a1384-118">예제 3: 모든 운영 체제 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="a1384-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="a1384-119">이 명령은 모든 운영 체제 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="a1384-120">변수</span><span class="sxs-lookup"><span data-stu-id="a1384-120">PARAMETERS</span></span>

### <span data-ttu-id="a1384-121">-ID</span><span class="sxs-lookup"><span data-stu-id="a1384-121">-ID</span></span>
<span data-ttu-id="a1384-122">운영 체제 디스크의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-122">Specifies the unique ID of an operating system disk.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1384-123">-이름</span><span class="sxs-lookup"><span data-stu-id="a1384-123">-Name</span></span>
<span data-ttu-id="a1384-124">운영 체제 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-124">Specifies the name of an operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1384-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="a1384-125">-Profile</span></span>
<span data-ttu-id="a1384-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a1384-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a1384-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1384-128">CommonParameters</span></span>
<span data-ttu-id="a1384-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1384-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1384-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1384-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1384-131">입력</span><span class="sxs-lookup"><span data-stu-id="a1384-131">INPUTS</span></span>

## <span data-ttu-id="a1384-132">출력</span><span class="sxs-lookup"><span data-stu-id="a1384-132">OUTPUTS</span></span>

## <span data-ttu-id="a1384-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a1384-133">NOTES</span></span>

## <span data-ttu-id="a1384-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1384-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1384-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a1384-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


