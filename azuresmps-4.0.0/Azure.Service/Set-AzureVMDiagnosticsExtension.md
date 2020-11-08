---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A05B39BF-87EB-471E-9FCD-F7807CB46B4D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1aa7cff6d655bf33fa1a317516fda20237f6fc14
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046038"
---
# <span data-ttu-id="5869c-101">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5869c-101">Set-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5869c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5869c-102">SYNOPSIS</span></span>
<span data-ttu-id="5869c-103">가상 컴퓨터에서 Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-103">Configures the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5869c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5869c-104">SYNTAX</span></span>

### <span data-ttu-id="5869c-105">SetDiagnosticsExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="5869c-105">SetDiagnosticsExtension (Default)</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5869c-106">SetDiagnosticsWithReferenceExtension</span><span class="sxs-lookup"><span data-stu-id="5869c-106">SetDiagnosticsWithReferenceExtension</span></span>
```
Set-AzureVMDiagnosticsExtension [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [[-Version] <String>] [-Disable] [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5869c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5869c-107">DESCRIPTION</span></span>
<span data-ttu-id="5869c-108">**AzureVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Microsoft Azure 진단 확장을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-108">The **Set-AzureVMDiagnosticsExtension** cmdlet configures the Microsoft Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="5869c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5869c-109">EXAMPLES</span></span>

### <span data-ttu-id="5869c-110">예제 1: Azure 진단 확장을 적용 하 여 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="5869c-110">Example 1: Create a virtual machine with Azure Diagnostics extension applied</span></span>
```
PS C:\> $VM = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $VMImage
PS C:\> $VM = Add-AzureProvisioningConfig -VM $VM -AdminUsername $Username -Password $Password -Windows
PS C:\> $VM = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> New-AzureVM -Location $Location -ServiceName $Service_Name -VM $VM
```

<span data-ttu-id="5869c-111">이러한 명령을 사용 하면 가상 컴퓨터에서 Azure 진단 확장을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-111">These commands enable the Azure Diagnostics extension on a virtual machine.</span></span>

### <span data-ttu-id="5869c-112">예제 2: 기존 가상 컴퓨터에서 Azure 진단 확장 사용</span><span class="sxs-lookup"><span data-stu-id="5869c-112">Example 2: Enable an Azure Diagnostics extension on an existing virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName $Service_Name -Name $VM_Name
PS C:\> $VM_Update = Set-AzureVMDiagnosticsExtension -DiagnosticsConfigurationPath $Config_Path -Version "1.*" -VM $VM -StorageContext $Storage_Context
PS C:\> Update-AzureVM -ServiceName $Service_Name -Name $VM_Name -VM $VM_Update.VM
```

<span data-ttu-id="5869c-113">첫 번째 명령은 **get-add-azurevm** cmdlet을 사용 하 여 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-113">The first command uses the **Get-AzureVM** cmdlet to get a virtual machine.</span></span>

<span data-ttu-id="5869c-114">두 번째 명령은 **AzureVMDiagnosticsExtension** cmdlet을 사용 하 여 Azure 진단 확장을 포함 하도록 가상 컴퓨터 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-114">The second command uses the **Set-AzureVMDiagnosticsExtension** cmdlet to update the virtual machine configuration to include the Azure Diagnostics extension.</span></span>

<span data-ttu-id="5869c-115">마지막 명령은 업데이트 된 구성을 가상 컴퓨터에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-115">The final command applies the updated configuration to the virtual machine.</span></span>

## <span data-ttu-id="5869c-116">변수</span><span class="sxs-lookup"><span data-stu-id="5869c-116">PARAMETERS</span></span>

### <span data-ttu-id="5869c-117">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="5869c-117">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="5869c-118">진단 구성에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-118">Specifies a path for the diagnostics configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="5869c-119">-Disable</span></span>
<span data-ttu-id="5869c-120">이 cmdlet이 가상 컴퓨터에서 진단 확장을 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-120">Indicates that this cmdlet disables the diagnostics extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5869c-121">-InformationAction</span></span>
<span data-ttu-id="5869c-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5869c-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5869c-124">하기로</span><span class="sxs-lookup"><span data-stu-id="5869c-124">Continue</span></span>
- <span data-ttu-id="5869c-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="5869c-125">Ignore</span></span>
- <span data-ttu-id="5869c-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="5869c-126">Inquire</span></span>
- <span data-ttu-id="5869c-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5869c-127">SilentlyContinue</span></span>
- <span data-ttu-id="5869c-128">중지가</span><span class="sxs-lookup"><span data-stu-id="5869c-128">Stop</span></span>
- <span data-ttu-id="5869c-129">대기</span><span class="sxs-lookup"><span data-stu-id="5869c-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5869c-130">-InformationVariable</span></span>
<span data-ttu-id="5869c-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="5869c-132">-Profile</span></span>
<span data-ttu-id="5869c-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5869c-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="5869c-135">-ReferenceName</span></span>
<span data-ttu-id="5869c-136">진단 확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-136">Specifies the reference name for the diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: SetDiagnosticsWithReferenceExtension
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-137">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="5869c-137">-StorageAccountEndpoint</span></span>
<span data-ttu-id="5869c-138">저장소 계정 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-138">Specifies a storage account endpoint.</span></span>

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

### <span data-ttu-id="5869c-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5869c-139">-StorageAccountKey</span></span>
<span data-ttu-id="5869c-140">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-140">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5869c-141">-StorageAccountName</span></span>
<span data-ttu-id="5869c-142">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-142">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-143">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="5869c-143">-StorageContext</span></span>
<span data-ttu-id="5869c-144">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-144">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-145">-버전</span><span class="sxs-lookup"><span data-stu-id="5869c-145">-Version</span></span>
<span data-ttu-id="5869c-146">확장 버전을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-146">Specifies the extension version as a string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-147">-VM</span><span class="sxs-lookup"><span data-stu-id="5869c-147">-VM</span></span>
<span data-ttu-id="5869c-148">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-148">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5869c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5869c-149">CommonParameters</span></span>
<span data-ttu-id="5869c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5869c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5869c-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5869c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5869c-152">입력</span><span class="sxs-lookup"><span data-stu-id="5869c-152">INPUTS</span></span>

## <span data-ttu-id="5869c-153">출력</span><span class="sxs-lookup"><span data-stu-id="5869c-153">OUTPUTS</span></span>

## <span data-ttu-id="5869c-154">상속자</span><span class="sxs-lookup"><span data-stu-id="5869c-154">NOTES</span></span>

## <span data-ttu-id="5869c-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5869c-155">RELATED LINKS</span></span>

[<span data-ttu-id="5869c-156">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5869c-156">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5869c-157">제거-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5869c-157">Remove-AzureVMDiagnosticsExtension</span></span>](./Remove-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5869c-158">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5869c-158">Update-AzureVM</span></span>](./Update-AzureVM.md)


