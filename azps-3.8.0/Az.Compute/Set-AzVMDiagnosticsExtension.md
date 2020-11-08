---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5705d899f06d4a834b8864ec2a66c268e1c99c84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044637"
---
# <span data-ttu-id="68902-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68902-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="68902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68902-102">SYNOPSIS</span></span>
<span data-ttu-id="68902-103">가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="68902-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68902-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68902-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68902-105">DESCRIPTION</span></span>
<span data-ttu-id="68902-106">**AzVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="68902-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68902-107">EXAMPLES</span></span>

### <span data-ttu-id="68902-108">예제 1: 진단 구성 파일에 지정 된 저장소 계정을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="68902-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="68902-109">이 명령은 진단 구성 파일을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="68902-110">파일 diagnostics_publicconfig.xml에는 진단 데이터를 보낼 저장소 계정의 이름을 포함 하는 진단 확장에 대 한 공용 XML 구성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68902-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="68902-111">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="68902-112">예제 2: 저장소 계정 이름을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="68902-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="68902-113">이 명령은 저장소 계정 이름을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="68902-114">진단 구성에서 저장소 계정 이름을 지정 하지 않거나 구성 파일에 지정 된 진단 저장소 계정 이름을 재정의 하려는 경우 *Storageaccountname* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="68902-115">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="68902-116">예제 3: 저장소 계정 이름 및 키를 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="68902-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="68902-117">이 명령은 저장소 계정 이름과 키를 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="68902-118">진단 저장소 계정이 가상 컴퓨터와 다른 구독에 있는 경우 해당 이름 및 키를 명시적으로 지정 하 여 진단 데이터를 해당 저장소 계정에 보낼 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="68902-119">변수</span><span class="sxs-lookup"><span data-stu-id="68902-119">PARAMETERS</span></span>

### <span data-ttu-id="68902-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="68902-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="68902-121">이 cmdlet이 Azure 게스트 에이전트가 확장을 새 부 버전으로 자동 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="68902-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="68902-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68902-122">-DefaultProfile</span></span>
<span data-ttu-id="68902-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68902-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68902-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="68902-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="68902-125">구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="68902-126">-위치</span><span class="sxs-lookup"><span data-stu-id="68902-126">-Location</span></span>
<span data-ttu-id="68902-127">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="68902-128">-이름</span><span class="sxs-lookup"><span data-stu-id="68902-128">-Name</span></span>
<span data-ttu-id="68902-129">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="68902-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68902-130">-NoWait</span></span>
<span data-ttu-id="68902-131">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="68902-132">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="68902-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68902-133">-ResourceGroupName</span></span>
<span data-ttu-id="68902-134">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="68902-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="68902-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="68902-136">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-136">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="68902-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="68902-137">-StorageAccountKey</span></span>
<span data-ttu-id="68902-138">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-138">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="68902-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68902-139">-StorageAccountName</span></span>
<span data-ttu-id="68902-140">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-140">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="68902-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="68902-141">-StorageContext</span></span>
<span data-ttu-id="68902-142">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-142">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="68902-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="68902-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="68902-144">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="68902-145">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="68902-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="68902-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="68902-146">-VMName</span></span>
<span data-ttu-id="68902-147">이 cmdlet이 작동 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="68902-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68902-148">CommonParameters</span></span>
<span data-ttu-id="68902-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68902-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68902-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68902-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68902-151">입력</span><span class="sxs-lookup"><span data-stu-id="68902-151">INPUTS</span></span>

### <span data-ttu-id="68902-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="68902-152">System.String</span></span>

### <span data-ttu-id="68902-153">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="68902-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="68902-154">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="68902-154">System.Boolean</span></span>

## <span data-ttu-id="68902-155">출력</span><span class="sxs-lookup"><span data-stu-id="68902-155">OUTPUTS</span></span>

### <span data-ttu-id="68902-156">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="68902-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="68902-157">상속자</span><span class="sxs-lookup"><span data-stu-id="68902-157">NOTES</span></span>

## <span data-ttu-id="68902-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68902-158">RELATED LINKS</span></span>

[<span data-ttu-id="68902-159">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68902-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="68902-160">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="68902-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="68902-161">제거-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="68902-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


