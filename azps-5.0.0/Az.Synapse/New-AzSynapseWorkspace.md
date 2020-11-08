---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226009"
---
# <span data-ttu-id="03aa1-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="03aa1-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="03aa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03aa1-102">SYNOPSIS</span></span>
<span data-ttu-id="03aa1-103">Synapse Analytics 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="03aa1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03aa1-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03aa1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03aa1-105">DESCRIPTION</span></span>
<span data-ttu-id="03aa1-106">**AzSynapseWorkspace** Cmdlet은 Azure Synapse Analytics 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="03aa1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03aa1-107">EXAMPLES</span></span>

### <span data-ttu-id="03aa1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="03aa1-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="03aa1-109">이 명령은 ContosoResourceGroup 이라는 리소스 그룹에서 ContosoAdlGenStorage 데이터 저장소를 사용 하는 ContosoWorkspace 이라는 Synapse Analytics 작업 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="03aa1-110">변수</span><span class="sxs-lookup"><span data-stu-id="03aa1-110">PARAMETERS</span></span>

### <span data-ttu-id="03aa1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03aa1-111">-AsJob</span></span>
<span data-ttu-id="03aa1-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03aa1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03aa1-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="03aa1-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="03aa1-114">기본 ADLS Gen2 storage 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="03aa1-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="03aa1-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="03aa1-116">기본 ADLS Gen2 file 시스템입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="03aa1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03aa1-117">-DefaultProfile</span></span>
<span data-ttu-id="03aa1-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03aa1-119">-위치</span><span class="sxs-lookup"><span data-stu-id="03aa1-119">-Location</span></span>
<span data-ttu-id="03aa1-120">리소스를 만들어야 하는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="03aa1-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="03aa1-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="03aa1-122">Azure Synapse workspace 전용 Synapse 관리 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="03aa1-123">-이름</span><span class="sxs-lookup"><span data-stu-id="03aa1-123">-Name</span></span>
<span data-ttu-id="03aa1-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="03aa1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03aa1-125">-ResourceGroupName</span></span>
<span data-ttu-id="03aa1-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-126">Resource group name.</span></span>

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

### <span data-ttu-id="03aa1-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="03aa1-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="03aa1-128">SQL 관리자 자격 증명</span><span class="sxs-lookup"><span data-stu-id="03aa1-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="03aa1-129">태그</span><span class="sxs-lookup"><span data-stu-id="03aa1-129">-Tag</span></span>
<span data-ttu-id="03aa1-130">리소스와 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="03aa1-131">-확인</span><span class="sxs-lookup"><span data-stu-id="03aa1-131">-Confirm</span></span>
<span data-ttu-id="03aa1-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03aa1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03aa1-133">-WhatIf</span></span>
<span data-ttu-id="03aa1-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03aa1-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03aa1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03aa1-136">CommonParameters</span></span>
<span data-ttu-id="03aa1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03aa1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03aa1-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="03aa1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03aa1-139">입력</span><span class="sxs-lookup"><span data-stu-id="03aa1-139">INPUTS</span></span>

### <span data-ttu-id="03aa1-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03aa1-140">System.String</span></span>

### <span data-ttu-id="03aa1-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="03aa1-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03aa1-142">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="03aa1-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="03aa1-143">출력</span><span class="sxs-lookup"><span data-stu-id="03aa1-143">OUTPUTS</span></span>

### <span data-ttu-id="03aa1-144">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="03aa1-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="03aa1-145">상속자</span><span class="sxs-lookup"><span data-stu-id="03aa1-145">NOTES</span></span>

## <span data-ttu-id="03aa1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03aa1-146">RELATED LINKS</span></span>
