---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881142"
---
# <span data-ttu-id="79ab0-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="79ab0-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="79ab0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ab0-102">SYNOPSIS</span></span>
<span data-ttu-id="79ab0-103">스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79ab0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79ab0-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79ab0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79ab0-105">DESCRIPTION</span></span>
<span data-ttu-id="79ab0-106">**Get-AzureRmSnapshot** cmdlet은 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="79ab0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79ab0-107">EXAMPLES</span></span>

### <span data-ttu-id="79ab0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79ab0-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="79ab0-109">이 명령은 구독의 모든 스냅숏에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="79ab0-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="79ab0-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="79ab0-111">이 명령은 "ResourceGroupName1" 이라는 리소스 그룹에 있는 모든 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="79ab0-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="79ab0-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="79ab0-113">이 명령은 "ResourceGroupName1" 리소스 그룹에서 "SnapshotName1" 이름의 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="79ab0-114">변수</span><span class="sxs-lookup"><span data-stu-id="79ab0-114">PARAMETERS</span></span>

### <span data-ttu-id="79ab0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ab0-115">-DefaultProfile</span></span>
<span data-ttu-id="79ab0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ab0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ab0-117">-ResourceGroupName</span></span>
<span data-ttu-id="79ab0-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="79ab0-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="79ab0-119">-SnapshotName</span></span>
<span data-ttu-id="79ab0-120">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="79ab0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ab0-121">CommonParameters</span></span>
<span data-ttu-id="79ab0-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79ab0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ab0-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ab0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ab0-124">입력</span><span class="sxs-lookup"><span data-stu-id="79ab0-124">INPUTS</span></span>

### <span data-ttu-id="79ab0-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79ab0-125">System.String</span></span>

## <span data-ttu-id="79ab0-126">출력</span><span class="sxs-lookup"><span data-stu-id="79ab0-126">OUTPUTS</span></span>

### <span data-ttu-id="79ab0-127">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="79ab0-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="79ab0-128">상속자</span><span class="sxs-lookup"><span data-stu-id="79ab0-128">NOTES</span></span>

## <span data-ttu-id="79ab0-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79ab0-129">RELATED LINKS</span></span>

