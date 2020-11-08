---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045790"
---
# <span data-ttu-id="3831c-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3831c-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="3831c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3831c-102">SYNOPSIS</span></span>
<span data-ttu-id="3831c-103">가상 컴퓨터에서 Azure SQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="3831c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3831c-104">SYNTAX</span></span>

### <span data-ttu-id="3831c-105">EnableSqlServerExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="3831c-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3831c-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3831c-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3831c-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3831c-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3831c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3831c-108">DESCRIPTION</span></span>
<span data-ttu-id="3831c-109">**AzureVMSqlServerExtension** cmdlet은 가상 컴퓨터에서 Azure SQL Server 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="3831c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3831c-110">EXAMPLES</span></span>

### <span data-ttu-id="3831c-111">예제 1: 가상 컴퓨터에서 자동 패치 설정 설정</span><span class="sxs-lookup"><span data-stu-id="3831c-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="3831c-112">이 명령은 Azure 가상 컴퓨터에서 자동 패치 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="3831c-113">예제 2: 가상 컴퓨터에서 자동 백업 설정 설정</span><span class="sxs-lookup"><span data-stu-id="3831c-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="3831c-114">이 명령은 Azure 가상 컴퓨터에 대 한 자동 백업 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="3831c-115">예제 3: 가상 컴퓨터에서 SQL Server 확장 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="3831c-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="3831c-116">이 명령은 지정 된 가상 컴퓨터에서 SQL Server 가상 컴퓨터 확장을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="3831c-117">예제 4: 특정 가상 컴퓨터에서 SQL Server 확장 제거</span><span class="sxs-lookup"><span data-stu-id="3831c-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="3831c-118">이 명령은 VMName 이라는 가상 컴퓨터에서 SQL Server 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="3831c-119">변수</span><span class="sxs-lookup"><span data-stu-id="3831c-119">PARAMETERS</span></span>

### <span data-ttu-id="3831c-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="3831c-120">-AutoBackupSettings</span></span>
<span data-ttu-id="3831c-121">SQL Server 자동 백업 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="3831c-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="3831c-123">SQL Server 자동 패치 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-124">-Disable</span><span class="sxs-lookup"><span data-stu-id="3831c-124">-Disable</span></span>
<span data-ttu-id="3831c-125">이 cmdlet이 확장 상태를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3831c-126">-InformationAction</span></span>
<span data-ttu-id="3831c-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3831c-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3831c-129">하기로</span><span class="sxs-lookup"><span data-stu-id="3831c-129">Continue</span></span>
- <span data-ttu-id="3831c-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="3831c-130">Ignore</span></span>
- <span data-ttu-id="3831c-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="3831c-131">Inquire</span></span>
- <span data-ttu-id="3831c-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3831c-132">SilentlyContinue</span></span>
- <span data-ttu-id="3831c-133">중지가</span><span class="sxs-lookup"><span data-stu-id="3831c-133">Stop</span></span>
- <span data-ttu-id="3831c-134">대기</span><span class="sxs-lookup"><span data-stu-id="3831c-134">Suspend</span></span>

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

### <span data-ttu-id="3831c-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3831c-135">-InformationVariable</span></span>
<span data-ttu-id="3831c-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3831c-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="3831c-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="3831c-138">키 보관소 자격 증명 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="3831c-139">-Profile</span></span>
<span data-ttu-id="3831c-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3831c-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3831c-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="3831c-142">-ReferenceName</span></span>
<span data-ttu-id="3831c-143">SQL Server 확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-144">-제거</span><span class="sxs-lookup"><span data-stu-id="3831c-144">-Uninstall</span></span>
<span data-ttu-id="3831c-145">이 cmdlet이 가상 컴퓨터에서 SQL Server 확장을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3831c-146">-버전</span><span class="sxs-lookup"><span data-stu-id="3831c-146">-Version</span></span>
<span data-ttu-id="3831c-147">설정을 검색 하 Get-AzureVMSqlServerExtension는 SQL Server 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

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

### <span data-ttu-id="3831c-148">-VM</span><span class="sxs-lookup"><span data-stu-id="3831c-148">-VM</span></span>
<span data-ttu-id="3831c-149">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-149">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="3831c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3831c-150">CommonParameters</span></span>
<span data-ttu-id="3831c-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3831c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3831c-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3831c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3831c-153">입력</span><span class="sxs-lookup"><span data-stu-id="3831c-153">INPUTS</span></span>

## <span data-ttu-id="3831c-154">출력</span><span class="sxs-lookup"><span data-stu-id="3831c-154">OUTPUTS</span></span>

## <span data-ttu-id="3831c-155">상속자</span><span class="sxs-lookup"><span data-stu-id="3831c-155">NOTES</span></span>

## <span data-ttu-id="3831c-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3831c-156">RELATED LINKS</span></span>

[<span data-ttu-id="3831c-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3831c-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="3831c-158">제거-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3831c-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


