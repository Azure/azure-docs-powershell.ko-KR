---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495917"
---
# <span data-ttu-id="bbdfc-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bbdfc-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="bbdfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbdfc-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdfc-103">가상 머신에서 DSC 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="bbdfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="bbdfc-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdfc-105">설명</span><span class="sxs-lookup"><span data-stu-id="bbdfc-105">DESCRIPTION</span></span>
<span data-ttu-id="bbdfc-106">**Set-AzVMDscExtension** cmdlet은 리소스 그룹의 가상 Windows PowerShell DSC(Desired State Configuration) 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="bbdfc-107">예제</span><span class="sxs-lookup"><span data-stu-id="bbdfc-107">EXAMPLES</span></span>

### <span data-ttu-id="bbdfc-108">예제 1: DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="bbdfc-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="bbdfc-109">이 명령은 VM07이라는 가상 머신에서 DSC 확장을 설정하여 Stg Sample.ps1.zip 기본 컨테이너에서 다운로드할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="bbdfc-110">이 명령은 ConfigName이라는 구성을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="bbdfc-111">Sample.ps1.zip **Publish-AzVMDscConfiguration을** 사용하여 이전에 업로드했습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="bbdfc-112">예제 2: 구성 데이터를 사용하여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="bbdfc-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="bbdfc-113">이 명령은 VM13이라는 가상 머신의 확장을 설정하여 Stg라는 Sample.ps1.zip WindowsPowerShellDSC라는 컨테이너에서 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="bbdfc-114">ConfigName이라는 구성을 명령하고 구성 데이터 및 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="bbdfc-115">Sample.ps1.zip **Publish-AzVMDscConfiguration을** 사용하여 이전에 업로드했습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="bbdfc-116">예제 3: 자동 업데이트가 있는 구성 데이터를 사용하여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="bbdfc-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="bbdfc-117">이 명령은 VM22라는 가상 머신의 확장을 설정하여 Stg라는 Sample.ps1.zip WindowsPowerShellDSC라는 컨테이너에서 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="bbdfc-118">이 명령은 ConfigName이라는 구성을 호출하고 구성 데이터 및 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="bbdfc-119">또한 이 명령을 사용하면 확장 처리기에서 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="bbdfc-120">이 Sample.ps1.zip **Publish-AzVMDscConfiguration을** 사용하여 이전에 업로드했습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="bbdfc-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbdfc-121">PARAMETERS</span></span>

### <span data-ttu-id="bbdfc-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-122">-ArchiveBlobName</span></span>
<span data-ttu-id="bbdfc-123">이전에 Publish-AzVMDscConfiguration cmdlet에 의해 업로드된 구성 파일의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-124">-ArchiveContainerName</span></span>
<span data-ttu-id="bbdfc-125">구성 보관함이 있는 Azure 저장소 컨테이너의 종류 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="bbdfc-127">구성 보관 파일을 포함하는 저장소 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="bbdfc-128">저장소 계정과 가상 머신이 모두 동일한 리소스 그룹에 있는 경우 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="bbdfc-130">ArchiveBlobName을 다운로드하는 데 사용되는 Azure Storage 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="bbdfc-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="bbdfc-132">저장소 엔드포인트 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="bbdfc-133">-AutoUpdate</span></span>
<span data-ttu-id="bbdfc-134">Version 매개 변수로 지정된 확장 처리기 *버전을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="bbdfc-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="bbdfc-135">기본적으로 확장 처리기에는 자동 확장이 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="bbdfc-136">자동 *업데이트* 매개 변수를 사용하여 확장 처리기에서 사용 가능한 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="bbdfc-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="bbdfc-137">-ConfigurationArgument</span></span>
<span data-ttu-id="bbdfc-138">구성 함수에 대한 인수를 포함하는 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="bbdfc-139">-ConfigurationData</span></span>
<span data-ttu-id="bbdfc-140">구성에 대한 데이터를 지정하는 .psd1 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-141">-ConfigurationName</span></span>
<span data-ttu-id="bbdfc-142">DSC 확장이 호출하는 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="bbdfc-143">-DataCollection</span></span>
<span data-ttu-id="bbdfc-144">데이터 수집 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-144">Specifies the data collection type.</span></span>
<span data-ttu-id="bbdfc-145">이 매개 변수에 허용되는 값은 사용 및 사용 안 하도록 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdfc-146">-DefaultProfile</span></span>
<span data-ttu-id="bbdfc-147">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbdfc-148">-Force</span><span class="sxs-lookup"><span data-stu-id="bbdfc-148">-Force</span></span>
<span data-ttu-id="bbdfc-149">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bbdfc-150">-Location</span><span class="sxs-lookup"><span data-stu-id="bbdfc-150">-Location</span></span>
<span data-ttu-id="bbdfc-151">리소스 확장의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-152">-Name</span><span class="sxs-lookup"><span data-stu-id="bbdfc-152">-Name</span></span>
<span data-ttu-id="bbdfc-153">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="bbdfc-154">기본값은 Microsoft.Powershell.DSC입니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bbdfc-155">-NoWait</span></span>
<span data-ttu-id="bbdfc-156">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bbdfc-157">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bbdfc-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-158">-ResourceGroupName</span></span>
<span data-ttu-id="bbdfc-159">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-159">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-160">-Version</span><span class="sxs-lookup"><span data-stu-id="bbdfc-160">-Version</span></span>
<span data-ttu-id="bbdfc-161">설정을 적용하는 DSC 확장의 Set-AzVMDscExtension 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="bbdfc-162">-VMName</span></span>
<span data-ttu-id="bbdfc-163">DSC 확장 처리기가 설치된 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="bbdfc-164">-WmfVersion</span></span>
<span data-ttu-id="bbdfc-165">WMF 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-165">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbdfc-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdfc-166">-Confirm</span></span>
<span data-ttu-id="bbdfc-167">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdfc-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdfc-168">-WhatIf</span></span>
<span data-ttu-id="bbdfc-169">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bbdfc-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdfc-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdfc-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdfc-171">CommonParameters</span></span>
<span data-ttu-id="bbdfc-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdfc-173">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbdfc-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdfc-174">입력</span><span class="sxs-lookup"><span data-stu-id="bbdfc-174">INPUTS</span></span>

### <span data-ttu-id="bbdfc-175">System.String</span><span class="sxs-lookup"><span data-stu-id="bbdfc-175">System.String</span></span>

### <span data-ttu-id="bbdfc-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bbdfc-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bbdfc-177">출력</span><span class="sxs-lookup"><span data-stu-id="bbdfc-177">OUTPUTS</span></span>

### <span data-ttu-id="bbdfc-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bbdfc-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bbdfc-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bbdfc-179">NOTES</span></span>

## <span data-ttu-id="bbdfc-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbdfc-180">RELATED LINKS</span></span>

[<span data-ttu-id="bbdfc-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bbdfc-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="bbdfc-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="bbdfc-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="bbdfc-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="bbdfc-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


