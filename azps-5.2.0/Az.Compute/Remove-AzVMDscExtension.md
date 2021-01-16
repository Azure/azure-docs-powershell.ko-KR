---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363749"
---
# <span data-ttu-id="0d0ae-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d0ae-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="0d0ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0ae-103">리소스 그룹의 가상 머신에서 DSC 확장 처리기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="0d0ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d0ae-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d0ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="0d0ae-106">**Remove-AzVMDscExtension** cmdlet은 리소스 그룹의 가상 머신에서 DSC(Desired State Configuration) 확장 처리기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="0d0ae-107">예제</span><span class="sxs-lookup"><span data-stu-id="0d0ae-107">EXAMPLES</span></span>

### <span data-ttu-id="0d0ae-108">예제 1: DSC 확장 제거</span><span class="sxs-lookup"><span data-stu-id="0d0ae-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="0d0ae-109">이 명령은 VM07이라는 가상 머신에서 DSC라는 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="0d0ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d0ae-110">PARAMETERS</span></span>

### <span data-ttu-id="0d0ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0ae-111">-DefaultProfile</span></span>
<span data-ttu-id="0d0ae-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d0ae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0d0ae-113">-Name</span></span>
<span data-ttu-id="0d0ae-114">이 cmdlet에서 제거하는 DSC 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="0d0ae-115">Set-AzVMDscExtension cmdlet은 이 이름을 **Remove-AzVMDscExtension에서** 사용하는 기본값인 Microsoft.Powershell.DSC로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0ae-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0d0ae-116">-NoWait</span></span>
<span data-ttu-id="0d0ae-117">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="0d0ae-118">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="0d0ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d0ae-120">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0d0ae-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0d0ae-121">-VMName</span></span>
<span data-ttu-id="0d0ae-122">이 cmdlet이 DSC 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="0d0ae-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d0ae-123">-Confirm</span></span>
<span data-ttu-id="0d0ae-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0ae-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0ae-125">-WhatIf</span></span>
<span data-ttu-id="0d0ae-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d0ae-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d0ae-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d0ae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0ae-128">CommonParameters</span></span>
<span data-ttu-id="0d0ae-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0ae-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d0ae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0ae-131">입력</span><span class="sxs-lookup"><span data-stu-id="0d0ae-131">INPUTS</span></span>

### <span data-ttu-id="0d0ae-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0d0ae-132">System.String</span></span>

## <span data-ttu-id="0d0ae-133">출력</span><span class="sxs-lookup"><span data-stu-id="0d0ae-133">OUTPUTS</span></span>

### <span data-ttu-id="0d0ae-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d0ae-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0d0ae-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d0ae-135">NOTES</span></span>

## <span data-ttu-id="0d0ae-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d0ae-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d0ae-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d0ae-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="0d0ae-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="0d0ae-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


