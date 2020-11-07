---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877092"
---
# <span data-ttu-id="456cb-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="456cb-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="456cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="456cb-102">SYNOPSIS</span></span>
<span data-ttu-id="456cb-103">스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="456cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="456cb-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="456cb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="456cb-105">DESCRIPTION</span></span>
<span data-ttu-id="456cb-106">**Get-AzSnapshot** cmdlet은 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="456cb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="456cb-107">EXAMPLES</span></span>

### <span data-ttu-id="456cb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="456cb-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="456cb-109">이 명령은 구독의 모든 스냅숏에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="456cb-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="456cb-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="456cb-111">이 명령은 "ResourceGroupName1" 이라는 리소스 그룹에 있는 모든 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="456cb-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="456cb-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="456cb-113">이 명령은 "ResourceGroupName1" 리소스 그룹에서 "SnapshotName1" 이름의 스냅숏의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="456cb-114">변수</span><span class="sxs-lookup"><span data-stu-id="456cb-114">PARAMETERS</span></span>

### <span data-ttu-id="456cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="456cb-115">-DefaultProfile</span></span>
<span data-ttu-id="456cb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="456cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="456cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="456cb-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="456cb-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="456cb-119">-SnapshotName</span></span>
<span data-ttu-id="456cb-120">스냅숏의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="456cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456cb-121">CommonParameters</span></span>
<span data-ttu-id="456cb-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="456cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456cb-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456cb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456cb-124">입력</span><span class="sxs-lookup"><span data-stu-id="456cb-124">INPUTS</span></span>

### <span data-ttu-id="456cb-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="456cb-125">System.String</span></span>

## <span data-ttu-id="456cb-126">출력</span><span class="sxs-lookup"><span data-stu-id="456cb-126">OUTPUTS</span></span>

### <span data-ttu-id="456cb-127">Microsoft. a. a. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="456cb-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="456cb-128">상속자</span><span class="sxs-lookup"><span data-stu-id="456cb-128">NOTES</span></span>

## <span data-ttu-id="456cb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="456cb-129">RELATED LINKS</span></span>

