---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: ce49a011ba7e6c746c97e4b1aca6273d7d8b650d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359948"
---
# <span data-ttu-id="5db13-101">New-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5db13-101">New-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5db13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5db13-102">SYNOPSIS</span></span>
<span data-ttu-id="5db13-103">ANF 계정에 대한 새 ANF(Azure NetApp Files) 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-103">Creates a new Azure NetApp Files (ANF) backup policy for an ANF account.</span></span>

## <span data-ttu-id="5db13-104">구문</span><span class="sxs-lookup"><span data-stu-id="5db13-104">SYNTAX</span></span>

### <span data-ttu-id="5db13-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5db13-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>] [-WeeklyBackupsToKeep <Int32>]
 [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5db13-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db13-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackupPolicy -Name <String> [-Enabled] [-DailyBackupsToKeep <Int32>]
 [-WeeklyBackupsToKeep <Int32>] [-MonthlyBackupsToKeep <Int32>] [-YearlyBackupsToKeep <Int32>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5db13-107">설명</span><span class="sxs-lookup"><span data-stu-id="5db13-107">DESCRIPTION</span></span>
<span data-ttu-id="5db13-108">**New-AzNetAppFilesActiveDirectory** cmdlet은 ANF 계정에 대한 새 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new backup policy for an ANF account.</span></span>

## <span data-ttu-id="5db13-109">예제</span><span class="sxs-lookup"><span data-stu-id="5db13-109">EXAMPLES</span></span>

### <span data-ttu-id="5db13-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5db13-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyBackupPolicy" -Tag @{"tag1" = "tagValue"} -Enabled -DailyBackupsToKeep 1 -WeeklyBackupsToKeep 2 -MonthlyBackupsToKeep 2 -YearlyBackupsToKeep 1
```

<span data-ttu-id="5db13-111">이 명령은 "MyAccount"라는 ANF 계정에 대한 새 ANF 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-111">This command creates the new ANF backup policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="5db13-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5db13-112">PARAMETERS</span></span>

### <span data-ttu-id="5db13-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5db13-113">-AccountName</span></span>
<span data-ttu-id="5db13-114">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="5db13-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5db13-115">-AccountObject</span></span>
<span data-ttu-id="5db13-116">새 Backup 정책에 대한 계정 개체</span><span class="sxs-lookup"><span data-stu-id="5db13-116">The Account object for the new Backup Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-117">-DailyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="5db13-117">-DailyBackupsToKeep</span></span>
<span data-ttu-id="5db13-118">유지할 일일 백업 수</span><span class="sxs-lookup"><span data-stu-id="5db13-118">Daily backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db13-119">-DefaultProfile</span></span>
<span data-ttu-id="5db13-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db13-121">-Enabled</span><span class="sxs-lookup"><span data-stu-id="5db13-121">-Enabled</span></span>
<span data-ttu-id="5db13-122">정책을 사용할지 여부를 결정하는 속성</span><span class="sxs-lookup"><span data-stu-id="5db13-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="5db13-123">-Location</span><span class="sxs-lookup"><span data-stu-id="5db13-123">-Location</span></span>
<span data-ttu-id="5db13-124">리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="5db13-124">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-125">-MonthlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="5db13-125">-MonthlyBackupsToKeep</span></span>
<span data-ttu-id="5db13-126">유지할 월별 백업 수</span><span class="sxs-lookup"><span data-stu-id="5db13-126">Monthly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5db13-127">-Name</span></span>
<span data-ttu-id="5db13-128">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="5db13-128">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db13-129">-ResourceGroupName</span></span>
<span data-ttu-id="5db13-130">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="5db13-130">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="5db13-131">-Tag</span></span>
<span data-ttu-id="5db13-132">리소스 태그를 나타내는 해시테이블 배열</span><span class="sxs-lookup"><span data-stu-id="5db13-132">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-133">-WeeklyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="5db13-133">-WeeklyBackupsToKeep</span></span>
<span data-ttu-id="5db13-134">유지할 주간 백업 수</span><span class="sxs-lookup"><span data-stu-id="5db13-134">Weekly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-135">-YearlyBackupsToKeep</span><span class="sxs-lookup"><span data-stu-id="5db13-135">-YearlyBackupsToKeep</span></span>
<span data-ttu-id="5db13-136">유지할 연도당 백업 수</span><span class="sxs-lookup"><span data-stu-id="5db13-136">Yearly backups count to keep</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5db13-137">-Confirm</span></span>
<span data-ttu-id="5db13-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5db13-139">-WhatIf</span></span>
<span data-ttu-id="5db13-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5db13-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5db13-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db13-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db13-142">CommonParameters</span></span>
<span data-ttu-id="5db13-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5db13-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db13-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5db13-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db13-145">입력</span><span class="sxs-lookup"><span data-stu-id="5db13-145">INPUTS</span></span>

### <span data-ttu-id="5db13-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5db13-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5db13-147">출력</span><span class="sxs-lookup"><span data-stu-id="5db13-147">OUTPUTS</span></span>

### <span data-ttu-id="5db13-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5db13-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="5db13-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5db13-149">NOTES</span></span>

## <span data-ttu-id="5db13-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5db13-150">RELATED LINKS</span></span>
