---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531108"
---
# <span data-ttu-id="dfbfe-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="dfbfe-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="dfbfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbfe-103">디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfbfe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfbfe-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="dfbfe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dfbfe-105">DESCRIPTION</span></span>
<span data-ttu-id="dfbfe-106">**Get-AzureRmDisk** cmdlet은 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="dfbfe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dfbfe-107">EXAMPLES</span></span>

### <span data-ttu-id="dfbfe-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dfbfe-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="dfbfe-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dfbfe-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="dfbfe-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="dfbfe-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="dfbfe-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="dfbfe-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="dfbfe-113">이 명령은 구독 하는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="dfbfe-114">변수</span><span class="sxs-lookup"><span data-stu-id="dfbfe-114">PARAMETERS</span></span>

### <span data-ttu-id="dfbfe-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="dfbfe-115">-DiskName</span></span>
<span data-ttu-id="dfbfe-116">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="dfbfe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbfe-117">-ResourceGroupName</span></span>
<span data-ttu-id="dfbfe-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dfbfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbfe-119">CommonParameters</span></span>
<span data-ttu-id="dfbfe-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfbfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbfe-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbfe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbfe-122">입력</span><span class="sxs-lookup"><span data-stu-id="dfbfe-122">INPUTS</span></span>

### <span data-ttu-id="dfbfe-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfbfe-123">System.String</span></span>

## <span data-ttu-id="dfbfe-124">출력</span><span class="sxs-lookup"><span data-stu-id="dfbfe-124">OUTPUTS</span></span>

### <span data-ttu-id="dfbfe-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="dfbfe-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="dfbfe-126">상속자</span><span class="sxs-lookup"><span data-stu-id="dfbfe-126">NOTES</span></span>

## <span data-ttu-id="dfbfe-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfbfe-127">RELATED LINKS</span></span>

