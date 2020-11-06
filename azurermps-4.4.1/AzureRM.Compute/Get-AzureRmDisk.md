---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536448"
---
# <span data-ttu-id="cbe3c-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="cbe3c-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="cbe3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe3c-103">디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbe3c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbe3c-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbe3c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cbe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe3c-106">**Get-AzureRmDisk** cmdlet은 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="cbe3c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cbe3c-107">EXAMPLES</span></span>

### <span data-ttu-id="cbe3c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cbe3c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="cbe3c-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="cbe3c-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="cbe3c-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="cbe3c-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="cbe3c-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="cbe3c-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="cbe3c-113">이 명령은 구독 하는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="cbe3c-114">변수</span><span class="sxs-lookup"><span data-stu-id="cbe3c-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe3c-115">-DefaultProfile</span></span>
<span data-ttu-id="cbe3c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbe3c-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="cbe3c-117">-DiskName</span></span>
<span data-ttu-id="cbe3c-118">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="cbe3c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe3c-119">-ResourceGroupName</span></span>
<span data-ttu-id="cbe3c-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cbe3c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe3c-121">CommonParameters</span></span>
<span data-ttu-id="cbe3c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbe3c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe3c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe3c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe3c-124">입력</span><span class="sxs-lookup"><span data-stu-id="cbe3c-124">INPUTS</span></span>

### <span data-ttu-id="cbe3c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cbe3c-125">System.String</span></span>

## <span data-ttu-id="cbe3c-126">출력</span><span class="sxs-lookup"><span data-stu-id="cbe3c-126">OUTPUTS</span></span>

### <span data-ttu-id="cbe3c-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="cbe3c-127">System.Object</span></span>

## <span data-ttu-id="cbe3c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="cbe3c-128">NOTES</span></span>

## <span data-ttu-id="cbe3c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbe3c-129">RELATED LINKS</span></span>

