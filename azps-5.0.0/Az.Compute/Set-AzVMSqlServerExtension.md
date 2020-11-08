---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217490"
---
# <span data-ttu-id="59f18-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59f18-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="59f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f18-102">SYNOPSIS</span></span>
<span data-ttu-id="59f18-103">가상 컴퓨터에서 Azure SQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="59f18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59f18-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59f18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59f18-105">DESCRIPTION</span></span>
<span data-ttu-id="59f18-106">**AzVMSqlServerExtension** cmdlet은 가상 컴퓨터의 AzureSQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="59f18-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59f18-107">EXAMPLES</span></span>

### <span data-ttu-id="59f18-108">예제 1: 가상 컴퓨터에서 자동 패치 설정 설정</span><span class="sxs-lookup"><span data-stu-id="59f18-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="59f18-109">첫 번째 명령은 **New AzVMSqlServerAutoPatchingConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="59f18-110">명령은 $AutoPatchingConfig 변수에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="59f18-111">두 번째 명령은 Get-AzVM cmdlet을 사용 하 여 Service02 이라는 서비스에서 VirtualMachine11 라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="59f18-112">이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="59f18-113">현재 cmdlet은 가상 컴퓨터에 대 한 $AutoPatchingConfig에서 자동 패치 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="59f18-114">명령이 가상 컴퓨터를 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="59f18-115">예제 2: 가상 컴퓨터에서 자동 백업 설정 설정</span><span class="sxs-lookup"><span data-stu-id="59f18-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="59f18-116">첫 번째 명령은 **New AzVMSqlServerAutoBackupConfig** cmdlet을 사용 하 여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="59f18-117">명령은 $AutoBackupConfig 변수에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="59f18-118">두 번째 명령은 Service02 이라는 서비스에서 VirtualMachine11 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="59f18-119">현재 cmdlet은 가상 컴퓨터에 대 한 $AutoBackupConfig에서 자동 백업 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="59f18-120">명령이 가상 컴퓨터를 Update-AzVM cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="59f18-121">예제 3: 가상 컴퓨터에서 SQL Server 확장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="59f18-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="59f18-122">이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="59f18-123">이 명령은 해당 가상 컴퓨터에서 SQL Server 가상 컴퓨터 확장을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="59f18-124">예제 4: 특정 가상 컴퓨터에서 SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="59f18-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="59f18-125">이 명령은 Service03에 VirtualMachine08 이라는 가상 컴퓨터를 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="59f18-126">명령에서 해당 가상 컴퓨터의 SQL Server 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="59f18-127">변수</span><span class="sxs-lookup"><span data-stu-id="59f18-127">PARAMETERS</span></span>

### <span data-ttu-id="59f18-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="59f18-128">-AutoBackupSettings</span></span>
<span data-ttu-id="59f18-129">SQL Server 자동 백업 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="59f18-130">**AutoBackupSettings** 개체를 만들려면 New-AzVMSqlServerAutoBackupConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="59f18-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="59f18-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="59f18-132">SQL Server 자동 패치 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="59f18-133">**AutoPatchingSettings** 개체를 만들려면 New-AzVMSqlServerAutoPatchingConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="59f18-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f18-134">-DefaultProfile</span></span>
<span data-ttu-id="59f18-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59f18-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="59f18-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="59f18-137">-위치</span><span class="sxs-lookup"><span data-stu-id="59f18-137">-Location</span></span>
<span data-ttu-id="59f18-138">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="59f18-139">-이름</span><span class="sxs-lookup"><span data-stu-id="59f18-139">-Name</span></span>
<span data-ttu-id="59f18-140">확장 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="59f18-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f18-141">-ResourceGroupName</span></span>
<span data-ttu-id="59f18-142">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="59f18-143">-버전</span><span class="sxs-lookup"><span data-stu-id="59f18-143">-Version</span></span>
<span data-ttu-id="59f18-144">SQL Server 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="59f18-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="59f18-145">-VMName</span></span>
<span data-ttu-id="59f18-146">이 cmdlet에서 SQL Server 확장을 설정 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="59f18-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f18-147">CommonParameters</span></span>
<span data-ttu-id="59f18-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f18-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59f18-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f18-150">입력</span><span class="sxs-lookup"><span data-stu-id="59f18-150">INPUTS</span></span>

### <span data-ttu-id="59f18-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59f18-151">System.String</span></span>

### <span data-ttu-id="59f18-152">AutoPatchingSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="59f18-153">AutoBackupSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="59f18-154">KeyVaultCredentialSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="59f18-155">출력</span><span class="sxs-lookup"><span data-stu-id="59f18-155">OUTPUTS</span></span>

### <span data-ttu-id="59f18-156">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="59f18-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="59f18-157">상속자</span><span class="sxs-lookup"><span data-stu-id="59f18-157">NOTES</span></span>

## <span data-ttu-id="59f18-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59f18-158">RELATED LINKS</span></span>

[<span data-ttu-id="59f18-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="59f18-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="59f18-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59f18-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="59f18-161">새로운 AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="59f18-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="59f18-162">새로운 AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="59f18-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="59f18-163">제거-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="59f18-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="59f18-164">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="59f18-164">Update-AzVM</span></span>](./Update-AzVM.md)


