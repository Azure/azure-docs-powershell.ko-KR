---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: e79229053030fdd2c1ed8a8fae4fccee493972a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701229"
---
# <span data-ttu-id="821f2-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="821f2-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="821f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821f2-102">SYNOPSIS</span></span>
<span data-ttu-id="821f2-103">가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="821f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="821f2-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="821f2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="821f2-105">DESCRIPTION</span></span>
<span data-ttu-id="821f2-106">**AzVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="821f2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="821f2-107">EXAMPLES</span></span>

### <span data-ttu-id="821f2-108">예제 1: 진단 구성 파일에 지정 된 저장소 계정을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="821f2-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="821f2-109">이 명령은 진단 구성 파일을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="821f2-110">파일 diagnostics_publicconfig.xml에는 진단 데이터를 보낼 저장소 계정의 이름을 포함 하는 진단 확장에 대 한 공용 XML 구성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="821f2-111">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="821f2-112">예제 2: 저장소 계정 이름을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="821f2-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="821f2-113">이 명령은 저장소 계정 이름을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="821f2-114">진단 구성에서 저장소 계정 이름을 지정 하지 않거나 구성 파일에 지정 된 진단 저장소 계정 이름을 재정의 하려는 경우 *Storageaccountname* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="821f2-115">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="821f2-116">예제 3: 저장소 계정 이름 및 키를 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="821f2-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="821f2-117">이 명령은 저장소 계정 이름과 키를 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="821f2-118">진단 저장소 계정이 가상 컴퓨터와 다른 구독에 있는 경우 해당 이름 및 키를 명시적으로 지정 하 여 진단 데이터를 해당 저장소 계정에 보낼 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="821f2-119">변수</span><span class="sxs-lookup"><span data-stu-id="821f2-119">PARAMETERS</span></span>

### <span data-ttu-id="821f2-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="821f2-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="821f2-121">이 cmdlet이 Azure 게스트 에이전트가 확장을 새 부 버전으로 자동 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

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

### <span data-ttu-id="821f2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821f2-122">-DefaultProfile</span></span>
<span data-ttu-id="821f2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="821f2-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="821f2-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="821f2-125">구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-125">Specifies the path of the configuration file.</span></span>

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

### <span data-ttu-id="821f2-126">-위치</span><span class="sxs-lookup"><span data-stu-id="821f2-126">-Location</span></span>
<span data-ttu-id="821f2-127">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-127">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="821f2-128">-이름</span><span class="sxs-lookup"><span data-stu-id="821f2-128">-Name</span></span>
<span data-ttu-id="821f2-129">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-129">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="821f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="821f2-131">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-131">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="821f2-132">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="821f2-132">-StorageAccountEndpoint</span></span>
<span data-ttu-id="821f2-133">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-133">Specifies the storage account endpoint.</span></span>

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

### <span data-ttu-id="821f2-134">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="821f2-134">-StorageAccountKey</span></span>
<span data-ttu-id="821f2-135">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-135">Specifies the storage account key.</span></span>

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

### <span data-ttu-id="821f2-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="821f2-136">-StorageAccountName</span></span>
<span data-ttu-id="821f2-137">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-137">Specifies the storage account name.</span></span>

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

### <span data-ttu-id="821f2-138">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="821f2-138">-StorageContext</span></span>
<span data-ttu-id="821f2-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-139">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="821f2-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="821f2-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="821f2-141">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-141">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="821f2-142">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="821f2-142">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="821f2-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="821f2-143">-VMName</span></span>
<span data-ttu-id="821f2-144">이 cmdlet이 작동 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-144">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="821f2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821f2-145">CommonParameters</span></span>
<span data-ttu-id="821f2-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821f2-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821f2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821f2-148">입력</span><span class="sxs-lookup"><span data-stu-id="821f2-148">INPUTS</span></span>

### <span data-ttu-id="821f2-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="821f2-149">System.String</span></span>

### <span data-ttu-id="821f2-150">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="821f2-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="821f2-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="821f2-151">System.Boolean</span></span>

## <span data-ttu-id="821f2-152">출력</span><span class="sxs-lookup"><span data-stu-id="821f2-152">OUTPUTS</span></span>

### <span data-ttu-id="821f2-153">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="821f2-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="821f2-154">상속자</span><span class="sxs-lookup"><span data-stu-id="821f2-154">NOTES</span></span>

## <span data-ttu-id="821f2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="821f2-155">RELATED LINKS</span></span>

[<span data-ttu-id="821f2-156">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="821f2-156">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="821f2-157">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="821f2-157">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="821f2-158">제거-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="821f2-158">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


