---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877093"
---
# <span data-ttu-id="7c143-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="7c143-101">Get-AzDisk</span></span>

## <span data-ttu-id="7c143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c143-102">SYNOPSIS</span></span>
<span data-ttu-id="7c143-103">관리 되는 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="7c143-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c143-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c143-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7c143-105">DESCRIPTION</span></span>
<span data-ttu-id="7c143-106">**AzDisk** Cmdlet은 관리 되는 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="7c143-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7c143-107">EXAMPLES</span></span>

### <span data-ttu-id="7c143-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c143-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="7c143-109">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 이름이 ' Disk01 ' 인 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7c143-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c143-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="7c143-111">이 명령은 리소스 그룹 ' ResourceGroup01 '에 있는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="7c143-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="7c143-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="7c143-113">이 명령은 구독 하는 모든 디스크의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="7c143-114">변수</span><span class="sxs-lookup"><span data-stu-id="7c143-114">PARAMETERS</span></span>

### <span data-ttu-id="7c143-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c143-115">-DefaultProfile</span></span>
<span data-ttu-id="7c143-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c143-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7c143-117">-DiskName</span></span>
<span data-ttu-id="7c143-118">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="7c143-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c143-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c143-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c143-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c143-121">CommonParameters</span></span>
<span data-ttu-id="7c143-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c143-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c143-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c143-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c143-124">입력</span><span class="sxs-lookup"><span data-stu-id="7c143-124">INPUTS</span></span>

### <span data-ttu-id="7c143-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c143-125">System.String</span></span>

## <span data-ttu-id="7c143-126">출력</span><span class="sxs-lookup"><span data-stu-id="7c143-126">OUTPUTS</span></span>

### <span data-ttu-id="7c143-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="7c143-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="7c143-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7c143-128">NOTES</span></span>

## <span data-ttu-id="7c143-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c143-129">RELATED LINKS</span></span>

