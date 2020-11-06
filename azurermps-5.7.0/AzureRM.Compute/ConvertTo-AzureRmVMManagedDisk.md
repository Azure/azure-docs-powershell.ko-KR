---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: bbfe3018cdf0560b7c7776217ceda7cfe7b77048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536092"
---
# <span data-ttu-id="ab9f6-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="ab9f6-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="ab9f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab9f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ab9f6-103">Blob 기반 디스크를 사용 하는 가상 컴퓨터를 관리 되는 디스크가 있는 가상 컴퓨터로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab9f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab9f6-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab9f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab9f6-105">DESCRIPTION</span></span>
<span data-ttu-id="ab9f6-106">**ConvertTo-AzureRmVMManagedDisk** cmdlet은 blob 기반 디스크를 사용 하는 가상 컴퓨터를 관리 되는 디스크가 있는 가상 컴퓨터로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="ab9f6-107">이 작업을 호출 하기 전에 가상 컴퓨터를 중지 하 고 할당을 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="ab9f6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ab9f6-108">EXAMPLES</span></span>

### <span data-ttu-id="ab9f6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab9f6-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="ab9f6-110">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 ' VM01 ' (이) 라는 가상 머신의 blob 기반 디스크를 관리 디스크로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="ab9f6-111">변수</span><span class="sxs-lookup"><span data-stu-id="ab9f6-111">PARAMETERS</span></span>

### <span data-ttu-id="ab9f6-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab9f6-112">-ResourceGroupName</span></span>
<span data-ttu-id="ab9f6-113">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-113">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9f6-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="ab9f6-114">-VMName</span></span>
<span data-ttu-id="ab9f6-115">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab9f6-116">-확인</span><span class="sxs-lookup"><span data-stu-id="ab9f6-116">-Confirm</span></span>
<span data-ttu-id="ab9f6-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9f6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab9f6-118">-WhatIf</span></span>
<span data-ttu-id="ab9f6-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab9f6-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab9f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab9f6-121">CommonParameters</span></span>
<span data-ttu-id="ab9f6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab9f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab9f6-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab9f6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab9f6-124">입력</span><span class="sxs-lookup"><span data-stu-id="ab9f6-124">INPUTS</span></span>

### <span data-ttu-id="ab9f6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ab9f6-125">System.String</span></span>

## <span data-ttu-id="ab9f6-126">출력</span><span class="sxs-lookup"><span data-stu-id="ab9f6-126">OUTPUTS</span></span>

### <span data-ttu-id="ab9f6-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ab9f6-127">System.Object</span></span>

## <span data-ttu-id="ab9f6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ab9f6-128">NOTES</span></span>

## <span data-ttu-id="ab9f6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab9f6-129">RELATED LINKS</span></span>

