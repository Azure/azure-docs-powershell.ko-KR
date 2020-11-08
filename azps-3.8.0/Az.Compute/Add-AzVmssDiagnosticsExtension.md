---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044904"
---
# <span data-ttu-id="53a3a-101">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="53a3a-101">Add-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="53a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="53a3a-103">VMSS에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-103">Adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="53a3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53a3a-104">SYNTAX</span></span>

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53a3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="53a3a-106">**AzVmssDiagnosticsExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-106">The **Add-AzVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="53a3a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53a3a-107">EXAMPLES</span></span>

### <span data-ttu-id="53a3a-108">예제 1: VMSS에 진단 확장 추가</span><span class="sxs-lookup"><span data-stu-id="53a3a-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="53a3a-109">이 명령은 VMSS에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="53a3a-110">변수</span><span class="sxs-lookup"><span data-stu-id="53a3a-110">PARAMETERS</span></span>

### <span data-ttu-id="53a3a-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="53a3a-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="53a3a-112">이 cmdlet이 Azure 게스트 에이전트가 확장을 새 부 버전으로 자동 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="53a3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a3a-113">-DefaultProfile</span></span>
<span data-ttu-id="53a3a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53a3a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="53a3a-115">-Force</span></span>
<span data-ttu-id="53a3a-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53a3a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="53a3a-117">-Name</span></span>
<span data-ttu-id="53a3a-118">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="53a3a-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="53a3a-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="53a3a-120">개인 구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="53a3a-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="53a3a-121">-SettingFilePath</span></span>
<span data-ttu-id="53a3a-122">공용 구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="53a3a-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="53a3a-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="53a3a-124">이 VMSS에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="53a3a-125">버전을 얻으려면 [AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 실행 하 고 *Type* 매개 변수에 대해 IaaSDiagnostics *Ername* 매개 변수에 대 한 진단 값을 사용 하 여 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="53a3a-125">To obtain the version, run the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="53a3a-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="53a3a-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="53a3a-127">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-127">Specify the VMSS object.</span></span>
<span data-ttu-id="53a3a-128">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="53a3a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="53a3a-129">-Confirm</span></span>
<span data-ttu-id="53a3a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53a3a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53a3a-131">-WhatIf</span></span>
<span data-ttu-id="53a3a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53a3a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53a3a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a3a-134">CommonParameters</span></span>
<span data-ttu-id="53a3a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53a3a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a3a-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53a3a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a3a-137">입력</span><span class="sxs-lookup"><span data-stu-id="53a3a-137">INPUTS</span></span>

### <span data-ttu-id="53a3a-138">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="53a3a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="53a3a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="53a3a-139">System.String</span></span>

### <span data-ttu-id="53a3a-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="53a3a-140">System.Boolean</span></span>

## <span data-ttu-id="53a3a-141">출력</span><span class="sxs-lookup"><span data-stu-id="53a3a-141">OUTPUTS</span></span>

### <span data-ttu-id="53a3a-142">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="53a3a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="53a3a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="53a3a-143">NOTES</span></span>

## <span data-ttu-id="53a3a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53a3a-144">RELATED LINKS</span></span>

[<span data-ttu-id="53a3a-145">추가-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="53a3a-145">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)

[<span data-ttu-id="53a3a-146">제거-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="53a3a-146">Remove-AzVmssDiagnosticsExtension</span></span>](./Remove-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="53a3a-147">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="53a3a-147">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)
