---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5b5a27be50da8a9c05b0cf766d48efe5844a0452
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009200"
---
# <span data-ttu-id="eb694-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb694-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="eb694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb694-102">SYNOPSIS</span></span>
<span data-ttu-id="eb694-103">가상 머신에서 진단 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="eb694-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb694-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb694-105">설명</span><span class="sxs-lookup"><span data-stu-id="eb694-105">DESCRIPTION</span></span>
<span data-ttu-id="eb694-106">**Remove-AzVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure Diagnostics 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="eb694-107">변경 내용을 구현하려면 이 cmdlet의 출력을 Update-AzVM cmdlet에 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="eb694-108">예제</span><span class="sxs-lookup"><span data-stu-id="eb694-108">EXAMPLES</span></span>

### <span data-ttu-id="eb694-109">예제 1: 가상 머신에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="eb694-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="eb694-110">이 명령은 ContosoVM22라는 가상 머신에서 진단 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="eb694-111">명령은 파이프라인 연산자를 사용하여 결과를 Update-AzVM cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb694-112">이 명령은 가상 머신을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="eb694-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eb694-113">PARAMETERS</span></span>

### <span data-ttu-id="eb694-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb694-114">-DefaultProfile</span></span>
<span data-ttu-id="eb694-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb694-116">-Name</span><span class="sxs-lookup"><span data-stu-id="eb694-116">-Name</span></span>
<span data-ttu-id="eb694-117">이 cmdlet이 제거하는 진단 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb694-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eb694-118">-NoWait</span></span>
<span data-ttu-id="eb694-119">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="eb694-120">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="eb694-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb694-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb694-122">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="eb694-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb694-123">-VMName</span></span>
<span data-ttu-id="eb694-124">이 cmdlet에서 진단 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb694-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb694-125">CommonParameters</span></span>
<span data-ttu-id="eb694-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb694-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb694-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb694-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb694-128">입력</span><span class="sxs-lookup"><span data-stu-id="eb694-128">INPUTS</span></span>

### <span data-ttu-id="eb694-129">System.String</span><span class="sxs-lookup"><span data-stu-id="eb694-129">System.String</span></span>

## <span data-ttu-id="eb694-130">출력</span><span class="sxs-lookup"><span data-stu-id="eb694-130">OUTPUTS</span></span>

### <span data-ttu-id="eb694-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb694-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eb694-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb694-132">NOTES</span></span>

## <span data-ttu-id="eb694-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb694-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb694-134">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb694-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="eb694-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="eb694-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="eb694-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="eb694-136">Update-AzVM</span></span>](./Update-AzVM.md)


