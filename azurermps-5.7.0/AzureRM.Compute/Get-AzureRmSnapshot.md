---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531104"
---
# <span data-ttu-id="36b30-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="36b30-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="36b30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36b30-102">SYNOPSIS</span></span>
<span data-ttu-id="36b30-103">스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36b30-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="36b30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="36b30-105">DESCRIPTION</span></span>
<span data-ttu-id="36b30-106">**Get-AzureRmSnapshot** cmdlet은 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="36b30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="36b30-107">EXAMPLES</span></span>

### <span data-ttu-id="36b30-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="36b30-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="36b30-109">이 명령은 구독의 모든 스냅숏에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="36b30-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="36b30-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="36b30-111">이 명령은 "ResourceGroupName1" 이라는 리소스 그룹에 있는 모든 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="36b30-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="36b30-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="36b30-113">이 명령은 "ResourceGroupName1" 리소스 그룹에서 "SnapshotName1" 이름의 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="36b30-114">변수</span><span class="sxs-lookup"><span data-stu-id="36b30-114">PARAMETERS</span></span>

### <span data-ttu-id="36b30-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b30-115">-ResourceGroupName</span></span>
<span data-ttu-id="36b30-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b30-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="36b30-117">-SnapshotName</span></span>
<span data-ttu-id="36b30-118">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b30-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b30-119">CommonParameters</span></span>
<span data-ttu-id="36b30-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36b30-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b30-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b30-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b30-122">입력</span><span class="sxs-lookup"><span data-stu-id="36b30-122">INPUTS</span></span>

### <span data-ttu-id="36b30-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="36b30-123">System.String</span></span>

## <span data-ttu-id="36b30-124">출력</span><span class="sxs-lookup"><span data-stu-id="36b30-124">OUTPUTS</span></span>

### <span data-ttu-id="36b30-125">System. 개체</span><span class="sxs-lookup"><span data-stu-id="36b30-125">System.Object</span></span>

## <span data-ttu-id="36b30-126">상속자</span><span class="sxs-lookup"><span data-stu-id="36b30-126">NOTES</span></span>

## <span data-ttu-id="36b30-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36b30-127">RELATED LINKS</span></span>

