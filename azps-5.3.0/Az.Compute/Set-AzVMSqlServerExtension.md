---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495902"
---
# <span data-ttu-id="9ac5e-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ac5e-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="9ac5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac5e-103">가상 머신에서 Azure SQL Server 확장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="9ac5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ac5e-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ac5e-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac5e-106">**Set-AzVMSqlServerExtension** cmdlet은 가상 머신에서 AzureSQL 서버 확장을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="9ac5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="9ac5e-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac5e-108">예제 1: 가상 머신에서 자동 패치 설정 설정</span><span class="sxs-lookup"><span data-stu-id="9ac5e-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="9ac5e-109">첫 번째 명령은 **New-AzVMSqlServerAutoPatchingConfig** cmdlet을 사용하여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="9ac5e-110">이 명령은 구성을 $AutoPatchingConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="9ac5e-111">두 번째 명령은 Get-AzVM cmdlet을 사용하여 Service02라는 서비스에서 VirtualMachine11이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="9ac5e-112">이 명령은 파이프라인 연산자를 사용하여 해당 개체를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9ac5e-113">현재 cmdlet은 가상 머신에 대한 $AutoPatchingConfig 자동 패치 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="9ac5e-114">이 명령은 가상 머신을 Update-AzVM cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="9ac5e-115">예제 2: 가상 머신에서 자동 백업 설정 설정</span><span class="sxs-lookup"><span data-stu-id="9ac5e-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="9ac5e-116">첫 번째 명령은 **New-AzVMSqlServerAutoBackupConfig** cmdlet을 사용하여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="9ac5e-117">이 명령은 구성을 $AutoBackupConfig 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="9ac5e-118">두 번째 명령은 Service02라는 서비스에서 VirtualMachine11이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9ac5e-119">현재 cmdlet은 가상 머신에 대한 $AutoBackupConfig 백업 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="9ac5e-120">이 명령은 가상 머신을 Update-AzVM cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="9ac5e-121">예제 3: 가상 SQL Server 확장을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="9ac5e-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="9ac5e-122">이 명령은 Service03에서 VirtualMachine08이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9ac5e-123">이 명령은 SQL Server 가상 머신 확장을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="9ac5e-124">예제 4: 특정 가상 SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="9ac5e-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="9ac5e-125">이 명령은 Service03에서 VirtualMachine08이라는 가상 머신을 얻은 다음 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9ac5e-126">이 명령은 가상 머신에 SQL Server 가상 머신 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="9ac5e-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ac5e-127">PARAMETERS</span></span>

### <span data-ttu-id="9ac5e-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-128">-AutoBackupSettings</span></span>
<span data-ttu-id="9ac5e-129">자동 백업 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="9ac5e-130">**AutoBackupSettings** 개체를 만들 경우 New-AzVMSqlServerAutoBackupConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac5e-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="9ac5e-132">자동 패치 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="9ac5e-133">**AutoPatchingSettings** 개체를 만들 New-AzVMSqlServerAutoPatchingConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac5e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac5e-134">-DefaultProfile</span></span>
<span data-ttu-id="9ac5e-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ac5e-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-136">-KeyVaultCredentialSettings</span></span>
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac5e-137">-Location</span><span class="sxs-lookup"><span data-stu-id="9ac5e-137">-Location</span></span>
<span data-ttu-id="9ac5e-138">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-138">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac5e-139">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac5e-139">-Name</span></span>
<span data-ttu-id="9ac5e-140">확장에 대한 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="9ac5e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac5e-141">-ResourceGroupName</span></span>
<span data-ttu-id="9ac5e-142">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9ac5e-143">-Version</span><span class="sxs-lookup"><span data-stu-id="9ac5e-143">-Version</span></span>
<span data-ttu-id="9ac5e-144">확장의 버전을 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-144">Specifies the version of the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac5e-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="9ac5e-145">-VMName</span></span>
<span data-ttu-id="9ac5e-146">이 cmdlet이 확장을 설정하는 가상 머신의 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="9ac5e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac5e-147">CommonParameters</span></span>
<span data-ttu-id="9ac5e-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac5e-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ac5e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac5e-150">입력</span><span class="sxs-lookup"><span data-stu-id="9ac5e-150">INPUTS</span></span>

### <span data-ttu-id="9ac5e-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9ac5e-151">System.String</span></span>

### <span data-ttu-id="9ac5e-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="9ac5e-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="9ac5e-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="9ac5e-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="9ac5e-155">출력</span><span class="sxs-lookup"><span data-stu-id="9ac5e-155">OUTPUTS</span></span>

### <span data-ttu-id="9ac5e-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ac5e-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9ac5e-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ac5e-157">NOTES</span></span>

## <span data-ttu-id="9ac5e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac5e-158">RELATED LINKS</span></span>

[<span data-ttu-id="9ac5e-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ac5e-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9ac5e-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ac5e-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="9ac5e-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="9ac5e-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="9ac5e-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="9ac5e-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="9ac5e-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9ac5e-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="9ac5e-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9ac5e-164">Update-AzVM</span></span>](./Update-AzVM.md)


