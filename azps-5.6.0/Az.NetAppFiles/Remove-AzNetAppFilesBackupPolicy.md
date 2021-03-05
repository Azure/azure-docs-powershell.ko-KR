---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: de9d0cf5d989cfa4d910f8e5ee9d959393c42632
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968331"
---
# <span data-ttu-id="ca226-101">Remove-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ca226-101">Remove-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ca226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca226-102">SYNOPSIS</span></span>
<span data-ttu-id="ca226-103">ANF(Azure NetApp Files) 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-103">Deletes an Azure NetApp Files (ANF) backup policy.</span></span>

## <span data-ttu-id="ca226-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca226-104">SYNTAX</span></span>

### <span data-ttu-id="ca226-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca226-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca226-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca226-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -Name <String> -AccountObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca226-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca226-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca226-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca226-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesBackupPolicy -InputObject <PSNetAppFilesBackupPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca226-109">설명</span><span class="sxs-lookup"><span data-stu-id="ca226-109">DESCRIPTION</span></span>
<span data-ttu-id="ca226-110">**Remove-AzNetAppFilesBackupPolicy** cmdlet은 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-110">The **Remove-AzNetAppFilesBackupPolicy** cmdlet deletes an ANF backup policy.</span></span>

## <span data-ttu-id="ca226-111">예제</span><span class="sxs-lookup"><span data-stu-id="ca226-111">EXAMPLES</span></span>

### <span data-ttu-id="ca226-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ca226-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="ca226-113">이 명령은 "MyAccount"에 대해 "MyBackupPolicy"라는 이름으로 새 ANF 백업 정책을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-113">This command deletes the new ANF backup policy with a the name "MyBackupPolicy" for account "MyAccount".</span></span>

## <span data-ttu-id="ca226-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca226-114">PARAMETERS</span></span>

### <span data-ttu-id="ca226-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ca226-115">-AccountName</span></span>
<span data-ttu-id="ca226-116">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="ca226-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ca226-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ca226-117">-AccountObject</span></span>
<span data-ttu-id="ca226-118">제거할 백업 정책이 포함된 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ca226-118">The Account object containing the Backup Policy to remove</span></span>

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

### <span data-ttu-id="ca226-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca226-119">-DefaultProfile</span></span>
<span data-ttu-id="ca226-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca226-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca226-121">-InputObject</span></span>
<span data-ttu-id="ca226-122">제거할 BackupPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="ca226-122">The BackupPolicy object to remove</span></span>

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

### <span data-ttu-id="ca226-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ca226-123">-Name</span></span>
<span data-ttu-id="ca226-124">ANF 백업 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="ca226-124">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="ca226-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca226-125">-PassThru</span></span>
<span data-ttu-id="ca226-126">지정된 백업 정책이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-126">Return whether the specified backup policy was successfully removed</span></span>

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

### <span data-ttu-id="ca226-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca226-127">-ResourceGroupName</span></span>
<span data-ttu-id="ca226-128">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ca226-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ca226-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca226-129">-ResourceId</span></span>
<span data-ttu-id="ca226-130">ANF Backup 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ca226-130">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="ca226-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ca226-131">-Confirm</span></span>
<span data-ttu-id="ca226-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca226-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca226-133">-WhatIf</span></span>
<span data-ttu-id="ca226-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca226-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca226-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca226-136">CommonParameters</span></span>
<span data-ttu-id="ca226-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca226-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca226-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca226-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca226-139">입력</span><span class="sxs-lookup"><span data-stu-id="ca226-139">INPUTS</span></span>

### <span data-ttu-id="ca226-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ca226-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ca226-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ca226-141">System.String</span></span>

### <span data-ttu-id="ca226-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ca226-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ca226-143">출력</span><span class="sxs-lookup"><span data-stu-id="ca226-143">OUTPUTS</span></span>

### <span data-ttu-id="ca226-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ca226-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ca226-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca226-145">NOTES</span></span>

## <span data-ttu-id="ca226-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca226-146">RELATED LINKS</span></span>
