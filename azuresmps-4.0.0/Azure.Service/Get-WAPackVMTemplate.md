---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047391"
---
# <span data-ttu-id="43e86-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="43e86-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="43e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43e86-102">SYNOPSIS</span></span>
<span data-ttu-id="43e86-103">가상 컴퓨터 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="43e86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43e86-104">SYNTAX</span></span>

### <span data-ttu-id="43e86-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="43e86-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="43e86-106">찡그린 Mid</span><span class="sxs-lookup"><span data-stu-id="43e86-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="43e86-107">FromName</span><span class="sxs-lookup"><span data-stu-id="43e86-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43e86-108">설명은</span><span class="sxs-lookup"><span data-stu-id="43e86-108">DESCRIPTION</span></span>
<span data-ttu-id="43e86-109">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="43e86-110">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="43e86-111">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="43e86-112">**Get-WAPackVMTemplate** cmdlet은 가상 컴퓨터 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="43e86-113">예제의</span><span class="sxs-lookup"><span data-stu-id="43e86-113">EXAMPLES</span></span>

### <span data-ttu-id="43e86-114">예제 1: 이름을 사용 하 여 가상 컴퓨터 서식 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="43e86-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="43e86-115">이 명령은 ContosoTemplate04 이라는 가상 컴퓨터 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="43e86-116">예제 2: ID를 사용 하 여 가상 컴퓨터 서식 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="43e86-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="43e86-117">이 명령은 지정 된 ID를 가진 가상 컴퓨터 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="43e86-118">예제 3: 모든 가상 컴퓨터 템플릿 가져오기</span><span class="sxs-lookup"><span data-stu-id="43e86-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="43e86-119">이 명령은 모든 가상 컴퓨터 템플릿을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="43e86-120">변수</span><span class="sxs-lookup"><span data-stu-id="43e86-120">PARAMETERS</span></span>

### <span data-ttu-id="43e86-121">-ID</span><span class="sxs-lookup"><span data-stu-id="43e86-121">-ID</span></span>
<span data-ttu-id="43e86-122">서식 파일의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-122">Specifies the unique ID of a template.</span></span>

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

### <span data-ttu-id="43e86-123">-이름</span><span class="sxs-lookup"><span data-stu-id="43e86-123">-Name</span></span>
<span data-ttu-id="43e86-124">서식 파일의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-124">Specifies the name of a template.</span></span>

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

### <span data-ttu-id="43e86-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="43e86-125">-Profile</span></span>
<span data-ttu-id="43e86-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43e86-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43e86-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e86-128">CommonParameters</span></span>
<span data-ttu-id="43e86-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43e86-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e86-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43e86-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e86-131">입력</span><span class="sxs-lookup"><span data-stu-id="43e86-131">INPUTS</span></span>

## <span data-ttu-id="43e86-132">출력</span><span class="sxs-lookup"><span data-stu-id="43e86-132">OUTPUTS</span></span>

## <span data-ttu-id="43e86-133">상속자</span><span class="sxs-lookup"><span data-stu-id="43e86-133">NOTES</span></span>

## <span data-ttu-id="43e86-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43e86-134">RELATED LINKS</span></span>

[<span data-ttu-id="43e86-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="43e86-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


