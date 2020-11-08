---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047353"
---
# <span data-ttu-id="31b78-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="31b78-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="31b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b78-102">SYNOPSIS</span></span>
<span data-ttu-id="31b78-103">클라우드 서비스 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="31b78-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b78-104">SYNTAX</span></span>

### <span data-ttu-id="31b78-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="31b78-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="31b78-106">FromName</span><span class="sxs-lookup"><span data-stu-id="31b78-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31b78-107">설명은</span><span class="sxs-lookup"><span data-stu-id="31b78-107">DESCRIPTION</span></span>
<span data-ttu-id="31b78-108">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="31b78-109">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="31b78-110">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="31b78-111">**Get-WAPackCloudService** cmdlet은 클라우드 서비스 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="31b78-112">예제의</span><span class="sxs-lookup"><span data-stu-id="31b78-112">EXAMPLES</span></span>

## <span data-ttu-id="31b78-113">변수</span><span class="sxs-lookup"><span data-stu-id="31b78-113">PARAMETERS</span></span>

### <span data-ttu-id="31b78-114">-이름</span><span class="sxs-lookup"><span data-stu-id="31b78-114">-Name</span></span>
<span data-ttu-id="31b78-115">클라우드 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="31b78-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="31b78-116">-Profile</span></span>
<span data-ttu-id="31b78-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31b78-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31b78-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b78-119">CommonParameters</span></span>
<span data-ttu-id="31b78-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b78-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b78-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b78-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b78-122">입력</span><span class="sxs-lookup"><span data-stu-id="31b78-122">INPUTS</span></span>

## <span data-ttu-id="31b78-123">출력</span><span class="sxs-lookup"><span data-stu-id="31b78-123">OUTPUTS</span></span>

## <span data-ttu-id="31b78-124">상속자</span><span class="sxs-lookup"><span data-stu-id="31b78-124">NOTES</span></span>

## <span data-ttu-id="31b78-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b78-125">RELATED LINKS</span></span>

[<span data-ttu-id="31b78-126">새로운 WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="31b78-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="31b78-127">제거-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="31b78-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


