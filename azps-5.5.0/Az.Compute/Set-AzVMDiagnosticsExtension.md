---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199172"
---
# <span data-ttu-id="1ee29-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ee29-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="1ee29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ee29-102">SYNOPSIS</span></span>
<span data-ttu-id="1ee29-103">가상 머신에서 Azure 진단 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1ee29-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ee29-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ee29-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ee29-105">DESCRIPTION</span></span>
<span data-ttu-id="1ee29-106">**Set-AzVMDiagnosticsExtension** cmdlet은 가상 머신에서 Azure 진단 확장을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="1ee29-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ee29-107">EXAMPLES</span></span>

### <span data-ttu-id="1ee29-108">예제 1: 진단 구성 파일에 지정된 저장소 계정을 사용하여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="1ee29-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="1ee29-109">이 명령은 진단 구성 파일을 사용하여 진단을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="1ee29-110">이 diagnostics_publicconfig.xml 파일에는 진단 데이터를 보낼 저장소 계정의 이름을 포함하여 진단 확장에 대한 공용 XML 구성이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="1ee29-111">진단 저장소 계정은 가상 머신과 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="1ee29-112">예제 2: 저장소 계정 이름을 사용하여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="1ee29-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="1ee29-113">이 명령은 저장소 계정 이름을 사용하여 진단을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="1ee29-114">진단 구성에서 스토리지 계정 이름을 지정하지 않는 경우 또는 구성 파일에 지정된 진단 스토리지 계정 이름을 다시 정의하려는 경우 *StorageAccountName* 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="1ee29-115">진단 저장소 계정은 가상 머신과 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="1ee29-116">예제 3: 저장소 계정 이름 및 키를 사용하여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="1ee29-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="1ee29-117">이 명령은 저장소 계정 이름 및 키를 사용하여 진단을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="1ee29-118">진단 저장소 계정이 가상 머신과 다른 구독에 있는 경우 해당 이름 및 키를 명시적으로 지정하여 진단 데이터를 해당 저장소 계정에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="1ee29-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ee29-119">PARAMETERS</span></span>

### <span data-ttu-id="1ee29-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1ee29-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1ee29-121">이 cmdlet을 통해 Azure 게스트 에이전트가 확장을 최신 부 버전으로 자동으로 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ee29-122">-DefaultProfile</span></span>
<span data-ttu-id="1ee29-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ee29-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="1ee29-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="1ee29-125">구성 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-126">-Location</span><span class="sxs-lookup"><span data-stu-id="1ee29-126">-Location</span></span>
<span data-ttu-id="1ee29-127">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1ee29-128">-Name</span></span>
<span data-ttu-id="1ee29-129">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ee29-130">-NoWait</span></span>
<span data-ttu-id="1ee29-131">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1ee29-132">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1ee29-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ee29-133">-ResourceGroupName</span></span>
<span data-ttu-id="1ee29-134">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1ee29-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ee29-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="1ee29-136">저장소 계정 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1ee29-137">-StorageAccountKey</span></span>
<span data-ttu-id="1ee29-138">저장소 계정 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ee29-139">-StorageAccountName</span></span>
<span data-ttu-id="1ee29-140">저장소 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1ee29-141">-StorageContext</span></span>
<span data-ttu-id="1ee29-142">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1ee29-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="1ee29-144">이 가상 머신에 사용할 확장 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1ee29-145">버전을 얻게 Get-AzVMExtensionImage *Type* 매개 변수에 대한 Microsoft.Compute 매개 변수 및 VMAccessAgent 값을 사용하여 Get-AzVMExtensionImage cmdlet을 *실행합니다.*</span><span class="sxs-lookup"><span data-stu-id="1ee29-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ee29-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ee29-146">-VMName</span></span>
<span data-ttu-id="1ee29-147">이 cmdlet이 작동하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1ee29-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ee29-148">CommonParameters</span></span>
<span data-ttu-id="1ee29-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ee29-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ee29-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ee29-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ee29-151">입력</span><span class="sxs-lookup"><span data-stu-id="1ee29-151">INPUTS</span></span>

### <span data-ttu-id="1ee29-152">System.String</span><span class="sxs-lookup"><span data-stu-id="1ee29-152">System.String</span></span>

### <span data-ttu-id="1ee29-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1ee29-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="1ee29-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ee29-154">System.Boolean</span></span>

## <span data-ttu-id="1ee29-155">출력</span><span class="sxs-lookup"><span data-stu-id="1ee29-155">OUTPUTS</span></span>

### <span data-ttu-id="1ee29-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ee29-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1ee29-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ee29-157">NOTES</span></span>

## <span data-ttu-id="1ee29-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ee29-158">RELATED LINKS</span></span>

[<span data-ttu-id="1ee29-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ee29-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="1ee29-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1ee29-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="1ee29-161">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1ee29-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


