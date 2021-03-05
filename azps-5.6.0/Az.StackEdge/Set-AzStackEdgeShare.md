---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: b127180b8eceea3c33ace0da86cfc700c1c7d113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967227"
---
# <span data-ttu-id="f1ac1-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f1ac1-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="f1ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ac1-103">디바이스에 대한 공유를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-103">Updates the share for a device.</span></span>

## <span data-ttu-id="f1ac1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1ac1-104">SYNTAX</span></span>

### <span data-ttu-id="f1ac1-105">SmbParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1ac1-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1ac1-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1ac1-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1ac1-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1ac1-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1ac1-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1ac1-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1ac1-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1ac1-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1ac1-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1ac1-111">설명</span><span class="sxs-lookup"><span data-stu-id="f1ac1-111">DESCRIPTION</span></span>
<span data-ttu-id="f1ac1-112">이 **Set-AzStackEdgeShare는** 액세스 권한을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="f1ac1-113">예제</span><span class="sxs-lookup"><span data-stu-id="f1ac1-113">EXAMPLES</span></span>

### <span data-ttu-id="f1ac1-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1ac1-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="f1ac1-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1ac1-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="f1ac1-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1ac1-116">PARAMETERS</span></span>

### <span data-ttu-id="f1ac1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1ac1-117">-AsJob</span></span>
<span data-ttu-id="f1ac1-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1ac1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1ac1-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="f1ac1-119">-ClientAccessRight</span></span>
<span data-ttu-id="f1ac1-120">clientIds에 대한 읽기/쓰기 액세스, ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="f1ac1-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ac1-121">-DefaultProfile</span></span>
<span data-ttu-id="f1ac1-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ac1-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f1ac1-123">-DeviceName</span></span>
<span data-ttu-id="f1ac1-124">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="f1ac1-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1ac1-125">-InputObject</span></span>
<span data-ttu-id="f1ac1-126">입력 개체</span><span class="sxs-lookup"><span data-stu-id="f1ac1-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f1ac1-127">-Name</span></span>
<span data-ttu-id="f1ac1-128">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="f1ac1-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ac1-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1ac1-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f1ac1-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ac1-131">-ResourceId</span></span>
<span data-ttu-id="f1ac1-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1ac1-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="f1ac1-133">-UserAccessRight</span></span>
<span data-ttu-id="f1ac1-134">SMB 공유 유형에 액세스하기 위해 기존 사용자 이름과 함께 액세스 권한을 제공합니다. 예: @(@{"Username"="user-name-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="f1ac1-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1ac1-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f1ac1-135">-Confirm</span></span>
<span data-ttu-id="f1ac1-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ac1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ac1-137">-WhatIf</span></span>
<span data-ttu-id="f1ac1-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1ac1-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ac1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ac1-140">CommonParameters</span></span>
<span data-ttu-id="f1ac1-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ac1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ac1-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1ac1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ac1-143">입력</span><span class="sxs-lookup"><span data-stu-id="f1ac1-143">INPUTS</span></span>

### <span data-ttu-id="f1ac1-144">System.String</span><span class="sxs-lookup"><span data-stu-id="f1ac1-144">System.String</span></span>

### <span data-ttu-id="f1ac1-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f1ac1-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f1ac1-146">출력</span><span class="sxs-lookup"><span data-stu-id="f1ac1-146">OUTPUTS</span></span>

### <span data-ttu-id="f1ac1-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="f1ac1-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="f1ac1-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1ac1-148">NOTES</span></span>

## <span data-ttu-id="f1ac1-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1ac1-149">RELATED LINKS</span></span>
