---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 975e451854a935034dc4ed508770f48e126807e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359836"
---
# <span data-ttu-id="572ab-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="572ab-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="572ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572ab-102">SYNOPSIS</span></span>
<span data-ttu-id="572ab-103">ANF(Azure NetApp Files) 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="572ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="572ab-104">SYNTAX</span></span>

### <span data-ttu-id="572ab-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="572ab-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572ab-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572ab-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572ab-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="572ab-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572ab-109">설명</span><span class="sxs-lookup"><span data-stu-id="572ab-109">DESCRIPTION</span></span>
<span data-ttu-id="572ab-110">**Remove-AzNetAppFilesBackupPolicy** cmdlet은 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="572ab-111">예제</span><span class="sxs-lookup"><span data-stu-id="572ab-111">EXAMPLES</span></span>

### <span data-ttu-id="572ab-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="572ab-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="572ab-113">이 명령은 "MyAccount" 계정에 대해 이름이 "MyBackupPolicy"인 새 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="572ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="572ab-114">PARAMETERS</span></span>

### <span data-ttu-id="572ab-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="572ab-115">-AccountName</span></span>
<span data-ttu-id="572ab-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="572ab-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="572ab-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="572ab-117">-AccountObject</span></span>
<span data-ttu-id="572ab-118">제거할 Backup 정책이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="572ab-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="572ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572ab-119">-DefaultProfile</span></span>
<span data-ttu-id="572ab-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="572ab-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="572ab-121">-InputObject</span></span>
<span data-ttu-id="572ab-122">제거할 BackupPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="572ab-122">The BackupPolicy object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-123">-Name</span><span class="sxs-lookup"><span data-stu-id="572ab-123">-Name</span></span>
<span data-ttu-id="572ab-124">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="572ab-124">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: BackupPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="572ab-125">-PassThru</span></span>
<span data-ttu-id="572ab-126">지정된 백업 정책이 성공적으로 제거됐는지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="572ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="572ab-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="572ab-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="572ab-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="572ab-129">-ResourceId</span></span>
<span data-ttu-id="572ab-130">ANF Backup 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="572ab-130">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="572ab-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="572ab-131">-Confirm</span></span>
<span data-ttu-id="572ab-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572ab-133">-WhatIf</span></span>
<span data-ttu-id="572ab-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="572ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572ab-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572ab-136">CommonParameters</span></span>
<span data-ttu-id="572ab-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="572ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572ab-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="572ab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572ab-139">입력</span><span class="sxs-lookup"><span data-stu-id="572ab-139">INPUTS</span></span>

### <span data-ttu-id="572ab-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="572ab-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="572ab-141">System.String</span><span class="sxs-lookup"><span data-stu-id="572ab-141">System.String</span></span>

### <span data-ttu-id="572ab-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="572ab-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="572ab-143">출력</span><span class="sxs-lookup"><span data-stu-id="572ab-143">OUTPUTS</span></span>

### <span data-ttu-id="572ab-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="572ab-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="572ab-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="572ab-145">NOTES</span></span>

## <span data-ttu-id="572ab-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="572ab-146">RELATED LINKS</span></span>
