---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047430"
---
# <span data-ttu-id="37c7d-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="37c7d-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="37c7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="37c7d-103">크기 프로필 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-103">Gets size profile objects.</span></span>

## <span data-ttu-id="37c7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37c7d-104">SYNTAX</span></span>

### <span data-ttu-id="37c7d-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="37c7d-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="37c7d-106">찡그린 Mid</span><span class="sxs-lookup"><span data-stu-id="37c7d-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="37c7d-107">FromName</span><span class="sxs-lookup"><span data-stu-id="37c7d-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="37c7d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37c7d-108">DESCRIPTION</span></span>
<span data-ttu-id="37c7d-109">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="37c7d-110">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="37c7d-111">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="37c7d-112">**Get-WAPackVMSizeProfile** cmdlet은 가상 컴퓨터의 크기 프로필 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="37c7d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="37c7d-113">EXAMPLES</span></span>

### <span data-ttu-id="37c7d-114">예제 1: 이름을 사용 하 여 크기 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="37c7d-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="37c7d-115">이 명령은 ContosoSizeProfile07 이라는 크기 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="37c7d-116">예제 2: ID를 사용 하 여 크기 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="37c7d-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="37c7d-117">이 명령은 지정 된 ID를 갖는 크기 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="37c7d-118">예제 3: 모든 크기 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="37c7d-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="37c7d-119">이 명령은 모든 크기 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="37c7d-120">변수</span><span class="sxs-lookup"><span data-stu-id="37c7d-120">PARAMETERS</span></span>

### <span data-ttu-id="37c7d-121">-ID</span><span class="sxs-lookup"><span data-stu-id="37c7d-121">-ID</span></span>
<span data-ttu-id="37c7d-122">크기 프로필의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="37c7d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="37c7d-123">-Name</span></span>
<span data-ttu-id="37c7d-124">크기 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="37c7d-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="37c7d-125">-Profile</span></span>
<span data-ttu-id="37c7d-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37c7d-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37c7d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c7d-128">CommonParameters</span></span>
<span data-ttu-id="37c7d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37c7d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c7d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c7d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c7d-131">입력</span><span class="sxs-lookup"><span data-stu-id="37c7d-131">INPUTS</span></span>

## <span data-ttu-id="37c7d-132">출력</span><span class="sxs-lookup"><span data-stu-id="37c7d-132">OUTPUTS</span></span>

## <span data-ttu-id="37c7d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="37c7d-133">NOTES</span></span>

## <span data-ttu-id="37c7d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37c7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="37c7d-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="37c7d-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


