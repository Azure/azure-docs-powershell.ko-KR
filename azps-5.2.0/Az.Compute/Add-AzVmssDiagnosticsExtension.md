---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353246"
---
# <span data-ttu-id="3f6c5-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3f6c5-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="3f6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6c5-103">VMSS에 진단 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="3f6c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f6c5-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f6c5-105">설명</span><span class="sxs-lookup"><span data-stu-id="3f6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="3f6c5-106">**Add-AzVmssDiagnosticsExtension** cmdlet은 VMSS(Virtual Machine Scale Set) 인스턴스에 진단 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3f6c5-107">예제</span><span class="sxs-lookup"><span data-stu-id="3f6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="3f6c5-108">예제 1: VMSS에 진단 확장 추가</span><span class="sxs-lookup"><span data-stu-id="3f6c5-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="3f6c5-109">이 명령은 VMSS에 진단 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="3f6c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f6c5-110">PARAMETERS</span></span>

### <span data-ttu-id="3f6c5-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3f6c5-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3f6c5-112">이 cmdlet을 통해 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6c5-113">-DefaultProfile</span></span>
<span data-ttu-id="3f6c5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f6c5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f6c5-115">-Force</span></span>
<span data-ttu-id="3f6c5-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f6c5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6c5-117">-Name</span></span>
<span data-ttu-id="3f6c5-118">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-118">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6c5-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="3f6c5-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="3f6c5-120">개인 구성 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="3f6c5-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="3f6c5-121">-SettingFilePath</span></span>
<span data-ttu-id="3f6c5-122">공용 구성 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="3f6c5-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3f6c5-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="3f6c5-124">이 VMSS에 사용할 확장 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="3f6c5-125">버전을 얻습니다. *PublisherName* 매개 변수에 대한 Microsoft.Azure.Diagnostics 값과 Type 매개 변수에 대한 IaaSDiagnostics 값을 사용하여 [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 *실행합니다.*</span><span class="sxs-lookup"><span data-stu-id="3f6c5-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6c5-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f6c5-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3f6c5-127">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-127">Specify the VMSS object.</span></span>
<span data-ttu-id="3f6c5-128">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f6c5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f6c5-129">-Confirm</span></span>
<span data-ttu-id="3f6c5-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f6c5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f6c5-131">-WhatIf</span></span>
<span data-ttu-id="3f6c5-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3f6c5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f6c5-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f6c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6c5-134">CommonParameters</span></span>
<span data-ttu-id="3f6c5-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6c5-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f6c5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6c5-137">입력</span><span class="sxs-lookup"><span data-stu-id="3f6c5-137">INPUTS</span></span>

### <span data-ttu-id="3f6c5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f6c5-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3f6c5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3f6c5-139">System.String</span></span>

### <span data-ttu-id="3f6c5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f6c5-140">System.Boolean</span></span>

## <span data-ttu-id="3f6c5-141">출력</span><span class="sxs-lookup"><span data-stu-id="3f6c5-141">OUTPUTS</span></span>

### <span data-ttu-id="3f6c5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f6c5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3f6c5-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f6c5-143">NOTES</span></span>

## <span data-ttu-id="3f6c5-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f6c5-144">RELATED LINKS</span></span>

[<span data-ttu-id="3f6c5-145">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3f6c5-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="3f6c5-146">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3f6c5-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="3f6c5-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="3f6c5-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
