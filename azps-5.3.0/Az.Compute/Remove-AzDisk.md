---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496019"
---
# <span data-ttu-id="f4d31-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="f4d31-101">Remove-AzDisk</span></span>

## <span data-ttu-id="f4d31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4d31-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d31-103">디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-103">Removes a disk.</span></span>

## <span data-ttu-id="f4d31-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4d31-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d31-105">설명</span><span class="sxs-lookup"><span data-stu-id="f4d31-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d31-106">**Remove-AzDisk** cmdlet은 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="f4d31-107">예제</span><span class="sxs-lookup"><span data-stu-id="f4d31-107">EXAMPLES</span></span>

### <span data-ttu-id="f4d31-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4d31-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="f4d31-109">이 명령은 리소스 그룹 'ResourceGroup01'에서 'Disk01'이라는 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f4d31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4d31-110">PARAMETERS</span></span>

### <span data-ttu-id="f4d31-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4d31-111">-AsJob</span></span>
<span data-ttu-id="f4d31-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f4d31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d31-113">-DefaultProfile</span></span>
<span data-ttu-id="f4d31-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d31-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="f4d31-115">-DiskName</span></span>
<span data-ttu-id="f4d31-116">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d31-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f4d31-117">-Force</span></span>
<span data-ttu-id="f4d31-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f4d31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d31-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4d31-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d31-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4d31-121">-Confirm</span></span>
<span data-ttu-id="f4d31-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d31-123">-WhatIf</span></span>
<span data-ttu-id="f4d31-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f4d31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d31-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d31-126">CommonParameters</span></span>
<span data-ttu-id="f4d31-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4d31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d31-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4d31-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d31-129">입력</span><span class="sxs-lookup"><span data-stu-id="f4d31-129">INPUTS</span></span>

### <span data-ttu-id="f4d31-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f4d31-130">System.String</span></span>

## <span data-ttu-id="f4d31-131">출력</span><span class="sxs-lookup"><span data-stu-id="f4d31-131">OUTPUTS</span></span>

### <span data-ttu-id="f4d31-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f4d31-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f4d31-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4d31-133">NOTES</span></span>

## <span data-ttu-id="f4d31-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4d31-134">RELATED LINKS</span></span>
