---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/disable-azurermvmdiskencryption
schema: 2.0.0
ms.openlocfilehash: 81b6d88dcdf5e5e5b41dfd8205cf137a37c9c47c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880570"
---
# <span data-ttu-id="2779c-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2779c-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="2779c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2779c-102">SYNOPSIS</span></span>
<span data-ttu-id="2779c-103">IaaS 가상 머신에서 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2779c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2779c-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2779c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2779c-105">DESCRIPTION</span></span>
<span data-ttu-id="2779c-106">**AzureRmVMDiskEncryption** Cmdlet은 IaaS (인프라 as services) 가상 컴퓨터로 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="2779c-107">이 cmdlet은 Windows 가상 컴퓨터와 Linux 가상 컴퓨터 에서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="2779c-108">이 cmdlet은 암호화를 사용 하지 않도록 가상 컴퓨터에 확장을 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="2779c-109">*Name* 매개 변수를 지정 하지 않으면 기본 이름인 "AzureDiskEncryption 암호화 Windows vm"이 있는 확장이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="2779c-110">주의:이 cmdlet은 가상 컴퓨터를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="2779c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2779c-111">EXAMPLES</span></span>

### <span data-ttu-id="2779c-112">예제 1: Windows 가상 컴퓨터의 모든 볼륨에 대해 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2779c-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="2779c-113">이 명령은 Group001 이라는 리소스 그룹에 속하는 가상 컴퓨터 VM002의 모두 유형의 볼륨에 대해 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="2779c-114">지 수 *etype* 매개 변수를 지정 하지 않았으므로 cmdlet은 값을 All로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="2779c-115">예제 2: Windows 가상 컴퓨터에서 데이터 볼륨에 대 한 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="2779c-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="2779c-116">이 명령은 Group002 이라는 리소스 그룹에 속하는 가상 컴퓨터 VM004의 형식 데이터 볼륨에 대 한 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="2779c-117">변수</span><span class="sxs-lookup"><span data-stu-id="2779c-117">PARAMETERS</span></span>

### <span data-ttu-id="2779c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2779c-118">-DefaultProfile</span></span>
<span data-ttu-id="2779c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2779c-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2779c-121">이 cmdlet이 확장의 부 버전에 대 한 자동 업그레이드를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-122">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="2779c-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="2779c-123">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-123">The extension publisher name.</span></span> <span data-ttu-id="2779c-124">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="2779c-125">-ExtensionType</span></span>
<span data-ttu-id="2779c-126">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-126">The extension type.</span></span> <span data-ttu-id="2779c-127">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-128">-Force</span><span class="sxs-lookup"><span data-stu-id="2779c-128">-Force</span></span>
<span data-ttu-id="2779c-129">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-130">-이름</span><span class="sxs-lookup"><span data-stu-id="2779c-130">-Name</span></span>
<span data-ttu-id="2779c-131">확장명을 나타내는 ARM (Azure Resource Manager) 리소스의 이름을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="2779c-132">이 매개 변수를 지정 하지 않으면이 cmdlet은 "Windows Vm 용 AzureDiskEncryption"을 기본값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2779c-133">-ResourceGroupName</span></span>
<span data-ttu-id="2779c-134">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="2779c-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2779c-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="2779c-136">암호화 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="2779c-137">이 매개 변수에 대 한 값을 지정 하지 않으면 최신 버전의 확장을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="2779c-138">-VMName</span></span>
<span data-ttu-id="2779c-139">이 cmdlet이 암호화를 사용 하지 않도록 설정 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="2779c-140">-가이 Etype</span><span class="sxs-lookup"><span data-stu-id="2779c-140">-VolumeType</span></span>
<span data-ttu-id="2779c-141">암호화 작업을 수행할 가상 컴퓨터 볼륨의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="2779c-142">Windows 가상 컴퓨터의 경우 유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="2779c-143">모든</span><span class="sxs-lookup"><span data-stu-id="2779c-143">All</span></span>
- <span data-ttu-id="2779c-144">변경할</span><span class="sxs-lookup"><span data-stu-id="2779c-144">OS</span></span>
- <span data-ttu-id="2779c-145">데이터.</span><span class="sxs-lookup"><span data-stu-id="2779c-145">Data.</span></span>
<span data-ttu-id="2779c-146">이 매개 변수에 대 한 값을 지정 하지 않으면 기본적으로 모두 값이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="2779c-147">현재 Linux에 대해 암호화 사용 안 함이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-148">-확인</span><span class="sxs-lookup"><span data-stu-id="2779c-148">-Confirm</span></span>
<span data-ttu-id="2779c-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2779c-150">-WhatIf</span></span>
<span data-ttu-id="2779c-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2779c-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2779c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2779c-153">CommonParameters</span></span>
<span data-ttu-id="2779c-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2779c-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2779c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2779c-156">입력</span><span class="sxs-lookup"><span data-stu-id="2779c-156">INPUTS</span></span>

### <span data-ttu-id="2779c-157">않아야</span><span class="sxs-lookup"><span data-stu-id="2779c-157">None</span></span>
<span data-ttu-id="2779c-158">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2779c-159">출력</span><span class="sxs-lookup"><span data-stu-id="2779c-159">OUTPUTS</span></span>

### <span data-ttu-id="2779c-160">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2779c-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2779c-161">상속자</span><span class="sxs-lookup"><span data-stu-id="2779c-161">NOTES</span></span>

## <span data-ttu-id="2779c-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2779c-162">RELATED LINKS</span></span>

[<span data-ttu-id="2779c-163">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2779c-163">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="2779c-164">제거-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2779c-164">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="2779c-165">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2779c-165">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


