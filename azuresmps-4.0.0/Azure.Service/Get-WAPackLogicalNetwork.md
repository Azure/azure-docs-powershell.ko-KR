---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047354"
---
# <span data-ttu-id="d3374-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="d3374-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="d3374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3374-102">SYNOPSIS</span></span>
<span data-ttu-id="d3374-103">논리 네트워크 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-103">Gets logical network objects.</span></span>

## <span data-ttu-id="d3374-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3374-104">SYNTAX</span></span>

### <span data-ttu-id="d3374-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3374-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3374-106">FromName</span><span class="sxs-lookup"><span data-stu-id="d3374-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3374-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d3374-107">DESCRIPTION</span></span>
<span data-ttu-id="d3374-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="d3374-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d3374-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d3374-111">**Get-WAPackLogicalNetwork** cmdlet은 논리적 네트워크 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="d3374-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d3374-112">EXAMPLES</span></span>

### <span data-ttu-id="d3374-113">예제 1: 이름을 사용 하 여 논리 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3374-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="d3374-114">이 명령은 ContosoLogicalNetwork01 이라는 논리 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="d3374-115">예제 2: 모든 논리 네트워크 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3374-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="d3374-116">이 명령은 모든 논리 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="d3374-117">변수</span><span class="sxs-lookup"><span data-stu-id="d3374-117">PARAMETERS</span></span>

### <span data-ttu-id="d3374-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d3374-118">-Name</span></span>
<span data-ttu-id="d3374-119">논리 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="d3374-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="d3374-120">-Profile</span></span>
<span data-ttu-id="d3374-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3374-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3374-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3374-123">CommonParameters</span></span>
<span data-ttu-id="d3374-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3374-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3374-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3374-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3374-126">입력</span><span class="sxs-lookup"><span data-stu-id="d3374-126">INPUTS</span></span>

## <span data-ttu-id="d3374-127">출력</span><span class="sxs-lookup"><span data-stu-id="d3374-127">OUTPUTS</span></span>

## <span data-ttu-id="d3374-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d3374-128">NOTES</span></span>

## <span data-ttu-id="d3374-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3374-129">RELATED LINKS</span></span>

