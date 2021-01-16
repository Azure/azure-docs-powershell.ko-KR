---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368880"
---
# <span data-ttu-id="af2a9-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="af2a9-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="af2a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="af2a9-103">Azure 가상 머신을 다시이미지합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="af2a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="af2a9-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="af2a9-105">DESCRIPTION</span></span>
<span data-ttu-id="af2a9-106">**Invoke-AzVMReimage** cmdlet은 Azure 가상 머신을 다시 이식합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="af2a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="af2a9-107">EXAMPLES</span></span>

### <span data-ttu-id="af2a9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="af2a9-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="af2a9-109">이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 다시 이식합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="af2a9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af2a9-110">PARAMETERS</span></span>

### <span data-ttu-id="af2a9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af2a9-111">-AsJob</span></span>
<span data-ttu-id="af2a9-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="af2a9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="af2a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2a9-113">-DefaultProfile</span></span>
<span data-ttu-id="af2a9-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af2a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="af2a9-116">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="af2a9-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="af2a9-117">-TempDisk</span></span>
<span data-ttu-id="af2a9-118">임시 디스크를 다시IMAGE할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="af2a9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="af2a9-119">-VMName</span></span>
<span data-ttu-id="af2a9-120">가상 머신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="af2a9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af2a9-121">-Confirm</span></span>
<span data-ttu-id="af2a9-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af2a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2a9-123">-WhatIf</span></span>
<span data-ttu-id="af2a9-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af2a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2a9-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af2a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2a9-126">CommonParameters</span></span>
<span data-ttu-id="af2a9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af2a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2a9-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af2a9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2a9-129">입력</span><span class="sxs-lookup"><span data-stu-id="af2a9-129">INPUTS</span></span>

### <span data-ttu-id="af2a9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="af2a9-130">System.String</span></span>

## <span data-ttu-id="af2a9-131">출력</span><span class="sxs-lookup"><span data-stu-id="af2a9-131">OUTPUTS</span></span>

### <span data-ttu-id="af2a9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="af2a9-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="af2a9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af2a9-133">NOTES</span></span>

## <span data-ttu-id="af2a9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af2a9-134">RELATED LINKS</span></span>
