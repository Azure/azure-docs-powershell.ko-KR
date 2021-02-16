---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187881"
---
# <span data-ttu-id="3dfe6-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3dfe6-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="3dfe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfe6-103">디바이스에 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="3dfe6-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dfe6-104">SYNTAX</span></span>

### <span data-ttu-id="3dfe6-105">SmbParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3dfe6-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dfe6-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfe6-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dfe6-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfe6-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dfe6-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dfe6-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dfe6-109">설명</span><span class="sxs-lookup"><span data-stu-id="3dfe6-109">DESCRIPTION</span></span>
<span data-ttu-id="3dfe6-110">**New-AzStackEdgeShare** cmdlet은 Stack Edge 디바이스에 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="3dfe6-111">예제</span><span class="sxs-lookup"><span data-stu-id="3dfe6-111">EXAMPLES</span></span>

### <span data-ttu-id="3dfe6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3dfe6-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="3dfe6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dfe6-113">PARAMETERS</span></span>

### <span data-ttu-id="3dfe6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dfe6-114">-AsJob</span></span>
<span data-ttu-id="3dfe6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3dfe6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dfe6-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="3dfe6-116">-ClientAccessRight</span></span>
<span data-ttu-id="3dfe6-117">clientIds에 대한 읽기/쓰기 액세스, 예:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="3dfe6-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="3dfe6-118">-CloudShare</span></span>
<span data-ttu-id="3dfe6-119">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="3dfe6-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3dfe6-120">-ContainerName</span></span>
<span data-ttu-id="3dfe6-121">컨테이너 이름(지정된 데이터 형식에 따라 Azure Files/Pageblob/블록 Blob의 이름을 나타)</span><span class="sxs-lookup"><span data-stu-id="3dfe6-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="3dfe6-122">-DataFormat</span></span>
<span data-ttu-id="3dfe6-123">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="3dfe6-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfe6-124">-DefaultProfile</span></span>
<span data-ttu-id="3dfe6-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dfe6-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3dfe6-126">-DeviceName</span></span>
<span data-ttu-id="3dfe6-127">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="3dfe6-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3dfe6-128">-Name</span></span>
<span data-ttu-id="3dfe6-129">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="3dfe6-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="3dfe6-130">-NFS</span></span>
<span data-ttu-id="3dfe6-131">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="3dfe6-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dfe6-132">-ResourceGroupName</span></span>
<span data-ttu-id="3dfe6-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3dfe6-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="3dfe6-134">-SMB</span></span>
<span data-ttu-id="3dfe6-135">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="3dfe6-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="3dfe6-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="3dfe6-137">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="3dfe6-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="3dfe6-138">-UserAccessRight</span></span>
<span data-ttu-id="3dfe6-139">기존 사용자 이름과 함께 SMB 공유 유형에 액세스할 수 있는 액세스 권한을 제공합니다. 예: @(@{"Username"="user-name-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="3dfe6-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfe6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dfe6-140">-Confirm</span></span>
<span data-ttu-id="3dfe6-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfe6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfe6-142">-WhatIf</span></span>
<span data-ttu-id="3dfe6-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3dfe6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dfe6-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfe6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfe6-145">CommonParameters</span></span>
<span data-ttu-id="3dfe6-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfe6-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3dfe6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfe6-148">입력</span><span class="sxs-lookup"><span data-stu-id="3dfe6-148">INPUTS</span></span>

### <span data-ttu-id="3dfe6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="3dfe6-149">System.String</span></span>

## <span data-ttu-id="3dfe6-150">출력</span><span class="sxs-lookup"><span data-stu-id="3dfe6-150">OUTPUTS</span></span>

### <span data-ttu-id="3dfe6-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3dfe6-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3dfe6-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3dfe6-152">NOTES</span></span>

## <span data-ttu-id="3dfe6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dfe6-153">RELATED LINKS</span></span>
