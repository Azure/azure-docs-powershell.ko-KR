---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: d49ff109a23a97f0c460ac56cd94b9c517f68dff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525696"
---
# <span data-ttu-id="925f0-101">Add-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="925f0-101">Add-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="925f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="925f0-102">SYNOPSIS</span></span>
<span data-ttu-id="925f0-103">VMSS에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-103">Adds a diagnostics extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="925f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="925f0-104">SYNTAX</span></span>

```
Add-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-SettingFilePath] <String> [[-ProtectedSettingFilePath] <String>] [[-Name] <String>]
 [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="925f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="925f0-105">DESCRIPTION</span></span>
<span data-ttu-id="925f0-106">**AzureRmVmssDiagnosticsExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-106">The **Add-AzureRmVmssDiagnosticsExtension** cmdlet adds a diagnostics extension to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="925f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="925f0-107">EXAMPLES</span></span>

### <span data-ttu-id="925f0-108">예제 1: VMSS에 진단 확장 추가</span><span class="sxs-lookup"><span data-stu-id="925f0-108">Example 1: Add a diagnostics extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

<span data-ttu-id="925f0-109">이 명령은 VMSS에 진단 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-109">This command adds a diagnostics extension to the VMSS.</span></span>

## <span data-ttu-id="925f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="925f0-110">PARAMETERS</span></span>

### <span data-ttu-id="925f0-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="925f0-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="925f0-112">이 cmdlet이 Azure 게스트 에이전트가 확장을 새 부 버전으로 자동 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-112">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="925f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925f0-113">-DefaultProfile</span></span>
<span data-ttu-id="925f0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="925f0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="925f0-115">-Force</span></span>
<span data-ttu-id="925f0-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="925f0-117">-이름</span><span class="sxs-lookup"><span data-stu-id="925f0-117">-Name</span></span>
<span data-ttu-id="925f0-118">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-118">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="925f0-119">-ProtectedSettingFilePath</span><span class="sxs-lookup"><span data-stu-id="925f0-119">-ProtectedSettingFilePath</span></span>
<span data-ttu-id="925f0-120">개인 구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-120">Specifies the path of the private configuration file.</span></span>

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

### <span data-ttu-id="925f0-121">-SettingFilePath</span><span class="sxs-lookup"><span data-stu-id="925f0-121">-SettingFilePath</span></span>
<span data-ttu-id="925f0-122">공용 구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-122">Specifies the path of the public configuration file.</span></span>

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

### <span data-ttu-id="925f0-123">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="925f0-123">-TypeHandlerVersion</span></span>
<span data-ttu-id="925f0-124">이 VMSS에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-124">Specifies the version of the extension to use for this VMSS.</span></span>
<span data-ttu-id="925f0-125">버전을 얻으려면 [AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 실행 하 고 *Type* 매개 변수에 대해 IaaSDiagnostics *Ername* 매개 변수에 대 한 진단 값을 사용 하 여 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="925f0-125">To obtain the version, run the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet with a value of Microsoft.Azure.Diagnostics for the *PublisherName* parameter and IaaSDiagnostics for the *Type* parameter.</span></span>

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

### <span data-ttu-id="925f0-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="925f0-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="925f0-127">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-127">Specify the VMSS object.</span></span>
<span data-ttu-id="925f0-128">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="925f0-129">-확인</span><span class="sxs-lookup"><span data-stu-id="925f0-129">-Confirm</span></span>
<span data-ttu-id="925f0-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="925f0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="925f0-131">-WhatIf</span></span>
<span data-ttu-id="925f0-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="925f0-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="925f0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925f0-134">CommonParameters</span></span>
<span data-ttu-id="925f0-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925f0-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="925f0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925f0-137">입력</span><span class="sxs-lookup"><span data-stu-id="925f0-137">INPUTS</span></span>

## <span data-ttu-id="925f0-138">출력</span><span class="sxs-lookup"><span data-stu-id="925f0-138">OUTPUTS</span></span>

###  
<span data-ttu-id="925f0-139">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="925f0-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="925f0-140">상속자</span><span class="sxs-lookup"><span data-stu-id="925f0-140">NOTES</span></span>

## <span data-ttu-id="925f0-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="925f0-141">RELATED LINKS</span></span>

[<span data-ttu-id="925f0-142">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="925f0-142">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)

[<span data-ttu-id="925f0-143">제거-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="925f0-143">Remove-AzureRmVmssDiagnosticsExtension</span></span>](./Remove-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="925f0-144">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="925f0-144">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)
