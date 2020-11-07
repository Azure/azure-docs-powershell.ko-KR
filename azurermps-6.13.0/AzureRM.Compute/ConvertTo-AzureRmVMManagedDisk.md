---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/convertto-azurermvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/ConvertTo-AzureRmVMManagedDisk.md
ms.openlocfilehash: 4aabd2a7b6e8b4b0b9037fc14189a0e14fdf8920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702798"
---
# <span data-ttu-id="417cc-101">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="417cc-101">ConvertTo-AzureRmVMManagedDisk</span></span>

## <span data-ttu-id="417cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="417cc-102">SYNOPSIS</span></span>
<span data-ttu-id="417cc-103">Blob 기반 디스크를 사용 하는 가상 컴퓨터를 관리 되는 디스크가 있는 가상 컴퓨터로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="417cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="417cc-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="417cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="417cc-105">DESCRIPTION</span></span>
<span data-ttu-id="417cc-106">**ConvertTo-AzureRmVMManagedDisk** cmdlet은 blob 기반 디스크를 사용 하는 가상 컴퓨터를 관리 되는 디스크가 있는 가상 컴퓨터로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-106">The **ConvertTo-AzureRmVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="417cc-107">이 작업을 호출 하기 전에 가상 컴퓨터를 중지 하 고 할당을 취소 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="417cc-108">예제의</span><span class="sxs-lookup"><span data-stu-id="417cc-108">EXAMPLES</span></span>

### <span data-ttu-id="417cc-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="417cc-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="417cc-110">이 명령은 리소스 그룹 ' ResourceGroup01 '에서 ' VM01 ' (이) 라는 가상 머신의 blob 기반 디스크를 관리 디스크로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="417cc-111">변수</span><span class="sxs-lookup"><span data-stu-id="417cc-111">PARAMETERS</span></span>

### <span data-ttu-id="417cc-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="417cc-112">-AsJob</span></span>
<span data-ttu-id="417cc-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="417cc-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417cc-114">-DefaultProfile</span></span>
<span data-ttu-id="417cc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="417cc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="417cc-116">-ResourceGroupName</span></span>
<span data-ttu-id="417cc-117">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417cc-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="417cc-118">-VMName</span></span>
<span data-ttu-id="417cc-119">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-119">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="417cc-120">-확인</span><span class="sxs-lookup"><span data-stu-id="417cc-120">-Confirm</span></span>
<span data-ttu-id="417cc-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417cc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="417cc-122">-WhatIf</span></span>
<span data-ttu-id="417cc-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="417cc-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="417cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417cc-125">CommonParameters</span></span>
<span data-ttu-id="417cc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="417cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417cc-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="417cc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417cc-128">입력</span><span class="sxs-lookup"><span data-stu-id="417cc-128">INPUTS</span></span>

### <span data-ttu-id="417cc-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="417cc-129">System.String</span></span>

## <span data-ttu-id="417cc-130">출력</span><span class="sxs-lookup"><span data-stu-id="417cc-130">OUTPUTS</span></span>

### <span data-ttu-id="417cc-131">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="417cc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="417cc-132">상속자</span><span class="sxs-lookup"><span data-stu-id="417cc-132">NOTES</span></span>

## <span data-ttu-id="417cc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="417cc-133">RELATED LINKS</span></span>
