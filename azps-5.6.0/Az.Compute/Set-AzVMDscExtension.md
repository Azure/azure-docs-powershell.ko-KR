---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: facd5a3637dcb1a8a392171468dd890279ba0f74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957504"
---
# <span data-ttu-id="d65c9-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d65c9-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="d65c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d65c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d65c9-103">가상 머신에서 DSC 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d65c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="d65c9-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d65c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="d65c9-105">DESCRIPTION</span></span>
<span data-ttu-id="d65c9-106">**Set-AzVMDscExtension** cmdlet은 리소스 그룹의 가상 머신에 Windows PowerShell DSC(원하는 상태 구성) 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="d65c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="d65c9-107">EXAMPLES</span></span>

### <span data-ttu-id="d65c9-108">예제 1: DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="d65c9-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d65c9-109">이 명령은 VM07이라는 가상 머신의 DSC 확장을 설정하여 Stg와 기본 컨테이너라는 Sample.ps1.zip 저장소 계정에서 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="d65c9-110">명령은 ConfigName이라는 구성을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="d65c9-111">이전에 Sample.ps1.zip **Publish-AzVMDscConfiguration** 을 사용하여 업로드된 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d65c9-112">예제 2: 구성 데이터를 사용하여 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="d65c9-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="d65c9-113">이 명령은 VM13이라는 가상 머신의 확장을 설정하여 Stg라는 Sample.ps1.zip WindowsPowerShellDSC라는 컨테이너에서 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d65c9-114">ConfigName이라는 구성을 명령하고 구성 데이터 및 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d65c9-115">이전에 Sample.ps1.zip **Publish-AzVMDscConfiguration** 을 사용하여 업로드된 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="d65c9-116">예제 3: 자동 업데이트가 있는 구성 데이터로 DSC 확장 설정</span><span class="sxs-lookup"><span data-stu-id="d65c9-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="d65c9-117">이 명령은 VM22라는 가상 머신의 확장을 설정하여 Stg라는 Sample.ps1.zip WindowsPowerShellDSC라는 컨테이너에서 확장을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="d65c9-118">명령은 ConfigName이라는 구성을 호출하고 구성 데이터 및 인수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="d65c9-119">또한 이 명령은 확장 처리기에서 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="d65c9-120">이전에 Sample.ps1.zip **Publish-AzVMDscConfiguration** 을 사용하여 업로드했습니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="d65c9-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d65c9-121">PARAMETERS</span></span>

### <span data-ttu-id="d65c9-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="d65c9-122">-ArchiveBlobName</span></span>
<span data-ttu-id="d65c9-123">이전에 cmdlet에서 업로드한 구성 파일의 이름을 Publish-AzVMDscConfiguration 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="d65c9-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="d65c9-124">-ArchiveContainerName</span></span>
<span data-ttu-id="d65c9-125">구성 보관소가 있는 Azure 저장소 컨테이너의 종 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="d65c9-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65c9-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="d65c9-127">구성 보관을 포함하는 저장소 계정을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="d65c9-128">저장소 계정과 가상 머신이 동일한 리소스 그룹에 있는 경우 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="d65c9-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d65c9-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="d65c9-130">ArchiveBlobName을 다운로드하는 데 사용되는 Azure Storage 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="d65c9-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="d65c9-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="d65c9-132">저장소 엔드포인트 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="d65c9-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="d65c9-133">-AutoUpdate</span></span>
<span data-ttu-id="d65c9-134">버전 매개 변수에 의해 지정된 확장 처리기 *버전을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="d65c9-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="d65c9-135">기본적으로 확장 처리기에서 자동 확장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="d65c9-136">*AutoUpdate* 매개 변수를 사용하여 확장 처리기에서 사용 가능한 경우를 최신 버전으로 자동 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="d65c9-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="d65c9-137">-ConfigurationArgument</span></span>
<span data-ttu-id="d65c9-138">구성 함수에 대한 인수를 포함하는 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="d65c9-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="d65c9-139">-ConfigurationData</span></span>
<span data-ttu-id="d65c9-140">구성에 대한 데이터를 지정하는 .psd1 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="d65c9-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d65c9-141">-ConfigurationName</span></span>
<span data-ttu-id="d65c9-142">DSC 확장이 호출하는 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="d65c9-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="d65c9-143">-DataCollection</span></span>
<span data-ttu-id="d65c9-144">데이터 수집 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-144">Specifies the data collection type.</span></span>
<span data-ttu-id="d65c9-145">이 매개 변수에 대해 허용되는 값은 사용 및 사용 안 하도록 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="d65c9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65c9-146">-DefaultProfile</span></span>
<span data-ttu-id="d65c9-147">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65c9-148">-Force</span><span class="sxs-lookup"><span data-stu-id="d65c9-148">-Force</span></span>
<span data-ttu-id="d65c9-149">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d65c9-150">-Location</span><span class="sxs-lookup"><span data-stu-id="d65c9-150">-Location</span></span>
<span data-ttu-id="d65c9-151">리소스 확장의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="d65c9-152">-Name</span><span class="sxs-lookup"><span data-stu-id="d65c9-152">-Name</span></span>
<span data-ttu-id="d65c9-153">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="d65c9-154">기본값은 Microsoft.Powershell.DSC입니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="d65c9-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d65c9-155">-NoWait</span></span>
<span data-ttu-id="d65c9-156">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="d65c9-157">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="d65c9-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65c9-158">-ResourceGroupName</span></span>
<span data-ttu-id="d65c9-159">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d65c9-160">-Version</span><span class="sxs-lookup"><span data-stu-id="d65c9-160">-Version</span></span>
<span data-ttu-id="d65c9-161">설정을 적용하는 DSC 확장의 Set-AzVMDscExtension 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="d65c9-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="d65c9-162">-VMName</span></span>
<span data-ttu-id="d65c9-163">DSC 확장 처리기가 설치된 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="d65c9-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="d65c9-164">-WmfVersion</span></span>
<span data-ttu-id="d65c9-165">WMF 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="d65c9-166">-확인</span><span class="sxs-lookup"><span data-stu-id="d65c9-166">-Confirm</span></span>
<span data-ttu-id="d65c9-167">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d65c9-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d65c9-168">-WhatIf</span></span>
<span data-ttu-id="d65c9-169">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d65c9-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d65c9-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65c9-171">CommonParameters</span></span>
<span data-ttu-id="d65c9-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d65c9-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65c9-173">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d65c9-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65c9-174">입력</span><span class="sxs-lookup"><span data-stu-id="d65c9-174">INPUTS</span></span>

### <span data-ttu-id="d65c9-175">System.String</span><span class="sxs-lookup"><span data-stu-id="d65c9-175">System.String</span></span>

### <span data-ttu-id="d65c9-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d65c9-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d65c9-177">출력</span><span class="sxs-lookup"><span data-stu-id="d65c9-177">OUTPUTS</span></span>

### <span data-ttu-id="d65c9-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d65c9-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d65c9-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d65c9-179">NOTES</span></span>

## <span data-ttu-id="d65c9-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d65c9-180">RELATED LINKS</span></span>

[<span data-ttu-id="d65c9-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d65c9-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="d65c9-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d65c9-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="d65c9-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d65c9-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


