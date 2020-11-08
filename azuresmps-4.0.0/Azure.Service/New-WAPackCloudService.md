---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047357"
---
# <span data-ttu-id="e49e2-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e49e2-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="e49e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e49e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e49e2-103">클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-103">Creates a cloud service.</span></span>

## <span data-ttu-id="e49e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e49e2-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e49e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e49e2-105">DESCRIPTION</span></span>
<span data-ttu-id="e49e2-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e49e2-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e49e2-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e49e2-109">**WAPackCloudService** cmdlet은 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="e49e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e49e2-110">EXAMPLES</span></span>

### <span data-ttu-id="e49e2-111">예제 1: 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="e49e2-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="e49e2-112">명령이 레이블이 있는 ContosoCloudService01 이라는 클라우드 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="e49e2-113">변수</span><span class="sxs-lookup"><span data-stu-id="e49e2-113">PARAMETERS</span></span>

### <span data-ttu-id="e49e2-114">-레이블</span><span class="sxs-lookup"><span data-stu-id="e49e2-114">-Label</span></span>
<span data-ttu-id="e49e2-115">클라우드 서비스에 대 한 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="e49e2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e49e2-116">-Name</span></span>
<span data-ttu-id="e49e2-117">Cloudservice의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="e49e2-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="e49e2-118">-Profile</span></span>
<span data-ttu-id="e49e2-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e49e2-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e49e2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49e2-121">CommonParameters</span></span>
<span data-ttu-id="e49e2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e49e2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49e2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49e2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49e2-124">입력</span><span class="sxs-lookup"><span data-stu-id="e49e2-124">INPUTS</span></span>

## <span data-ttu-id="e49e2-125">출력</span><span class="sxs-lookup"><span data-stu-id="e49e2-125">OUTPUTS</span></span>

## <span data-ttu-id="e49e2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e49e2-126">NOTES</span></span>

## <span data-ttu-id="e49e2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e49e2-127">RELATED LINKS</span></span>

[<span data-ttu-id="e49e2-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e49e2-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="e49e2-129">제거-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="e49e2-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


