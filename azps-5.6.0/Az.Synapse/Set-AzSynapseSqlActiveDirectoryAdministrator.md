---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992133"
---
# <span data-ttu-id="f9f2b-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="f9f2b-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="f9f2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f2b-103">Synapse Analytics 풀에 대한 Azure AD SQL 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="f9f2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9f2b-104">SYNTAX</span></span>

### <span data-ttu-id="f9f2b-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9f2b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9f2b-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9f2b-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9f2b-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9f2b-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f2b-108">설명</span><span class="sxs-lookup"><span data-stu-id="f9f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="f9f2b-109">**Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet은 현재 구독에서 Azure Synapse Analytics 작업 영역의 Azure AD(Azure Active Directory) 관리자를 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="f9f2b-110">한 번씩 하나의 관리자만 프로비전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="f9f2b-111">Azure AD의 다음 구성원을 Synapse Analytics 작업 영역 관리자로 프로비전할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="f9f2b-112">Azure AD의 네이티브 멤버</span><span class="sxs-lookup"><span data-stu-id="f9f2b-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="f9f2b-113">Azure AD의 페더리드 멤버</span><span class="sxs-lookup"><span data-stu-id="f9f2b-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="f9f2b-114">네이티브 또는 페더리드 멤버인 다른 Azure AD에서 가져온 멤버</span><span class="sxs-lookup"><span data-stu-id="f9f2b-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="f9f2b-115">보안 그룹으로 만든 Azure AD 그룹(예: Outlook.com, Hotmail.com 또는 Live.com 도메인의 경우)은 관리자 권한으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f9f2b-116">다른 게스트 계정(예: Gmail.com 또는 Yahoo.com)은 관리자 권한으로 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="f9f2b-117">관리자 권한으로 전용 Azure AD 그룹을 프로비전하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="f9f2b-118">예제</span><span class="sxs-lookup"><span data-stu-id="f9f2b-118">EXAMPLES</span></span>

### <span data-ttu-id="f9f2b-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9f2b-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="f9f2b-120">이 명령은 ContosoWorkspace라는 작업 영역의 DBAs라는 Azure AD 관리자 그룹을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f9f2b-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="f9f2b-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="f9f2b-122">이 명령은 ContosoWorkspace라는 작업 영역의 DBAs라는 Azure AD 관리자 그룹을 프로비전합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="f9f2b-123">이렇게 하면 그룹의 표시 이름이 고유하지 않은 경우에도 명령이 성공합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="f9f2b-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9f2b-124">PARAMETERS</span></span>

### <span data-ttu-id="f9f2b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9f2b-125">-AsJob</span></span>
<span data-ttu-id="f9f2b-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f9f2b-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9f2b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f2b-127">-DefaultProfile</span></span>
<span data-ttu-id="f9f2b-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f2b-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f9f2b-129">-DisplayName</span></span>
<span data-ttu-id="f9f2b-130">권한을 부여할 사용자 또는 그룹의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="f9f2b-131">이 표시 이름은 현재 구독과 연결된 활성 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9f2b-132">-InputObject</span></span>
<span data-ttu-id="f9f2b-133">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f9f2b-134">-ObjectId</span></span>
<span data-ttu-id="f9f2b-135">권한을 부여할 Azure Active Directory의 사용자 또는 그룹의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9f2b-136">-ResourceGroupName</span></span>
<span data-ttu-id="f9f2b-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9f2b-138">-ResourceId</span></span>
<span data-ttu-id="f9f2b-139">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9f2b-140">-WorkspaceName</span></span>
<span data-ttu-id="f9f2b-141">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f2b-142">-확인</span><span class="sxs-lookup"><span data-stu-id="f9f2b-142">-Confirm</span></span>
<span data-ttu-id="f9f2b-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f2b-144">-WhatIf</span></span>
<span data-ttu-id="f9f2b-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f2b-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f2b-147">CommonParameters</span></span>
<span data-ttu-id="f9f2b-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f2b-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9f2b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f2b-150">입력</span><span class="sxs-lookup"><span data-stu-id="f9f2b-150">INPUTS</span></span>

### <span data-ttu-id="f9f2b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9f2b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f9f2b-152">출력</span><span class="sxs-lookup"><span data-stu-id="f9f2b-152">OUTPUTS</span></span>

### <span data-ttu-id="f9f2b-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="f9f2b-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="f9f2b-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9f2b-154">NOTES</span></span>

## <span data-ttu-id="f9f2b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9f2b-155">RELATED LINKS</span></span>
