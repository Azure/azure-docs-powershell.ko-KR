---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: d93fd01fb178f093b6ed5527cca0c018cebe4f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531752"
---
# <span data-ttu-id="2bd48-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2bd48-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="2bd48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd48-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd48-103">가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bd48-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bd48-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [<CommonParameters>]
```

## <span data-ttu-id="2bd48-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2bd48-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd48-106">**AzureRmVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="2bd48-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2bd48-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd48-108">예제 1: 진단 구성 파일에 지정 된 저장소 계정을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="2bd48-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="2bd48-109">이 명령은 진단 구성 파일을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="2bd48-110">파일 diagnostics_publicconfig.xml에는 진단 데이터를 보낼 저장소 계정의 이름을 포함 하는 진단 확장에 대 한 공용 XML 구성이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="2bd48-111">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="2bd48-112">예제 2: 저장소 계정 이름을 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="2bd48-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="2bd48-113">이 명령은 저장소 계정 이름을 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="2bd48-114">진단 구성에서 저장소 계정 이름을 지정 하지 않거나 구성 파일에 지정 된 진단 저장소 계정 이름을 재정의 하려는 경우 *Storageaccountname* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="2bd48-115">진단 저장소 계정은 가상 컴퓨터와 동일한 구독에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="2bd48-116">예제 3: 저장소 계정 이름 및 키를 사용 하 여 진단 사용</span><span class="sxs-lookup"><span data-stu-id="2bd48-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="2bd48-117">이 명령은 저장소 계정 이름과 키를 사용 하 여 진단을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="2bd48-118">진단 저장소 계정이 가상 컴퓨터와 다른 구독에 있는 경우 해당 이름 및 키를 명시적으로 지정 하 여 진단 데이터를 해당 저장소 계정에 보낼 수 있도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="2bd48-119">변수</span><span class="sxs-lookup"><span data-stu-id="2bd48-119">PARAMETERS</span></span>

### <span data-ttu-id="2bd48-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2bd48-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2bd48-121">이 cmdlet이 Azure 게스트 에이전트가 확장을 새 부 버전으로 자동 업데이트할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="2bd48-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="2bd48-123">구성 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-123">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-124">-위치</span><span class="sxs-lookup"><span data-stu-id="2bd48-124">-Location</span></span>
<span data-ttu-id="2bd48-125">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-126">-이름</span><span class="sxs-lookup"><span data-stu-id="2bd48-126">-Name</span></span>
<span data-ttu-id="2bd48-127">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-127">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd48-128">-ResourceGroupName</span></span>
<span data-ttu-id="2bd48-129">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-130">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="2bd48-130">-StorageAccountEndpoint</span></span>
<span data-ttu-id="2bd48-131">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-131">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2bd48-132">-StorageAccountKey</span></span>
<span data-ttu-id="2bd48-133">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-133">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2bd48-134">-StorageAccountName</span></span>
<span data-ttu-id="2bd48-135">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-135">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-136">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2bd48-136">-StorageContext</span></span>
<span data-ttu-id="2bd48-137">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-137">Specifies the Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2bd48-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="2bd48-139">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2bd48-140">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzureRmVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="2bd48-140">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="2bd48-141">-VMName</span></span>
<span data-ttu-id="2bd48-142">이 cmdlet이 작동 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-142">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bd48-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd48-143">CommonParameters</span></span>
<span data-ttu-id="2bd48-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd48-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd48-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd48-146">입력</span><span class="sxs-lookup"><span data-stu-id="2bd48-146">INPUTS</span></span>

### <span data-ttu-id="2bd48-147">않아야</span><span class="sxs-lookup"><span data-stu-id="2bd48-147">None</span></span>
<span data-ttu-id="2bd48-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd48-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bd48-149">출력</span><span class="sxs-lookup"><span data-stu-id="2bd48-149">OUTPUTS</span></span>

## <span data-ttu-id="2bd48-150">상속자</span><span class="sxs-lookup"><span data-stu-id="2bd48-150">NOTES</span></span>

## <span data-ttu-id="2bd48-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bd48-151">RELATED LINKS</span></span>

[<span data-ttu-id="2bd48-152">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2bd48-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="2bd48-153">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="2bd48-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="2bd48-154">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2bd48-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


