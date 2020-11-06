---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 14b1c1179e9fee15f398c4518e446cf47396e660
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528596"
---
# <span data-ttu-id="d268d-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="d268d-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="d268d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d268d-102">SYNOPSIS</span></span>
<span data-ttu-id="d268d-103">스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d268d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d268d-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d268d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d268d-105">DESCRIPTION</span></span>
<span data-ttu-id="d268d-106">**Get-AzureRmSnapshot** cmdlet은 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="d268d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d268d-107">EXAMPLES</span></span>

### <span data-ttu-id="d268d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d268d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="d268d-109">이 명령은 구독의 모든 스냅숏에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="d268d-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="d268d-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="d268d-111">이 명령은 "ResourceGroupName1" 이라는 리소스 그룹에 있는 모든 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="d268d-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="d268d-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="d268d-113">이 명령은 "ResourceGroupName1" 리소스 그룹에서 "SnapshotName1" 이름의 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="d268d-114">변수</span><span class="sxs-lookup"><span data-stu-id="d268d-114">PARAMETERS</span></span>

### <span data-ttu-id="d268d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d268d-115">-DefaultProfile</span></span>
<span data-ttu-id="d268d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d268d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d268d-117">-ResourceGroupName</span></span>
<span data-ttu-id="d268d-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268d-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="d268d-119">-SnapshotName</span></span>
<span data-ttu-id="d268d-120">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d268d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d268d-121">CommonParameters</span></span>
<span data-ttu-id="d268d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d268d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d268d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d268d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d268d-124">입력</span><span class="sxs-lookup"><span data-stu-id="d268d-124">INPUTS</span></span>

### <span data-ttu-id="d268d-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d268d-125">System.String</span></span>

## <span data-ttu-id="d268d-126">출력</span><span class="sxs-lookup"><span data-stu-id="d268d-126">OUTPUTS</span></span>

### <span data-ttu-id="d268d-127">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="d268d-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="d268d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d268d-128">NOTES</span></span>

## <span data-ttu-id="d268d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d268d-129">RELATED LINKS</span></span>