---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: 28f1486375e0efc1f9b1b3f9a18f12050dafd799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002139"
---
# <span data-ttu-id="e3de3-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3de3-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="e3de3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3de3-102">SYNOPSIS</span></span>
<span data-ttu-id="e3de3-103">Synapse Analytics 작업 영역 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e3de3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3de3-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3de3-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3de3-105">DESCRIPTION</span></span>
<span data-ttu-id="e3de3-106">**New-AzSynapseWorkspace** cmdlet은 Azure Synapse Analytics 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="e3de3-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3de3-107">EXAMPLES</span></span>

### <span data-ttu-id="e3de3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3de3-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="e3de3-109">이 명령은 ContosoResourceGroup이라는 리소스 그룹에 ContosoAdlGenStorage Data Store를 사용하는 ContosoWorkspace라는 Synapse Analytics 작업 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="e3de3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3de3-110">PARAMETERS</span></span>

### <span data-ttu-id="e3de3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3de3-111">-AsJob</span></span>
<span data-ttu-id="e3de3-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e3de3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3de3-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3de3-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="e3de3-114">기본 ADLS Gen2 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="e3de3-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="e3de3-116">기본 ADLS Gen2 파일 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3de3-117">-DefaultProfile</span></span>
<span data-ttu-id="e3de3-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3de3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e3de3-119">-Location</span></span>
<span data-ttu-id="e3de3-120">리소스를 만들어야 하는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3de3-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="e3de3-122">Azure Synapse 작업 영역 전용 Synapse 관리 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="e3de3-123">-Name</span></span>
<span data-ttu-id="e3de3-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3de3-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3de3-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="e3de3-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="e3de3-128">SQL 자격 증명을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3de3-129">-Tag</span></span>
<span data-ttu-id="e3de3-130">문자열, 리소스와 연결된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3de3-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e3de3-131">-Confirm</span></span>
<span data-ttu-id="e3de3-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3de3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3de3-133">-WhatIf</span></span>
<span data-ttu-id="e3de3-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3de3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3de3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3de3-136">CommonParameters</span></span>
<span data-ttu-id="e3de3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3de3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3de3-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3de3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3de3-139">입력</span><span class="sxs-lookup"><span data-stu-id="e3de3-139">INPUTS</span></span>

### <span data-ttu-id="e3de3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e3de3-140">System.String</span></span>

### <span data-ttu-id="e3de3-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3de3-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e3de3-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="e3de3-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="e3de3-143">출력</span><span class="sxs-lookup"><span data-stu-id="e3de3-143">OUTPUTS</span></span>

### <span data-ttu-id="e3de3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e3de3-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e3de3-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3de3-145">NOTES</span></span>

## <span data-ttu-id="e3de3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3de3-146">RELATED LINKS</span></span>
