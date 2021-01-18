---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeShare.md
ms.openlocfilehash: 23dcfa42b1b7821e7d2c47b7b3c5e7d7b8579ed6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495688"
---
# <span data-ttu-id="d0122-101">New-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d0122-101">New-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="d0122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0122-102">SYNOPSIS</span></span>
<span data-ttu-id="d0122-103">디바이스에 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="d0122-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0122-104">SYNTAX</span></span>

### <span data-ttu-id="d0122-105">SmbParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d0122-105">SmbParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0122-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0122-106">CloudShareNfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0122-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0122-107">CloudShareSmbParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0122-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0122-108">NfsParameterSet</span></span>
```
New-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0122-109">설명</span><span class="sxs-lookup"><span data-stu-id="d0122-109">DESCRIPTION</span></span>
<span data-ttu-id="d0122-110">**New-AzDataBoxEdgeShare** cmdlet은 Data Box Edge 디바이스에 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-110">The **New-AzDataBoxEdgeShare** cmdlet creates a new share on the Data Box Edge device.</span></span>

## <span data-ttu-id="d0122-111">예제</span><span class="sxs-lookup"><span data-stu-id="d0122-111">EXAMPLES</span></span>

### <span data-ttu-id="d0122-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0122-112">Example 1</span></span>
```
PS C:\> New-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="d0122-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0122-113">PARAMETERS</span></span>

### <span data-ttu-id="d0122-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0122-114">-AsJob</span></span>
<span data-ttu-id="d0122-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d0122-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0122-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="d0122-116">-ClientAccessRight</span></span>
<span data-ttu-id="d0122-117">clientIds에 대한 읽기/쓰기 액세스, 예:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="d0122-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="d0122-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="d0122-118">-CloudShare</span></span>
<span data-ttu-id="d0122-119">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="d0122-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="d0122-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d0122-120">-ContainerName</span></span>
<span data-ttu-id="d0122-121">컨테이너 이름(지정된 데이터 형식에 따라 Azure Files/Pageblob/블록 Blob의 이름을 나타)</span><span class="sxs-lookup"><span data-stu-id="d0122-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="d0122-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="d0122-122">-DataFormat</span></span>
<span data-ttu-id="d0122-123">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="d0122-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="d0122-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0122-124">-DefaultProfile</span></span>
<span data-ttu-id="d0122-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0122-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d0122-126">-DeviceName</span></span>
<span data-ttu-id="d0122-127">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="d0122-127">Device Name</span></span>

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

### <span data-ttu-id="d0122-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d0122-128">-Name</span></span>
<span data-ttu-id="d0122-129">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="d0122-129">Resource Name</span></span>

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

### <span data-ttu-id="d0122-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="d0122-130">-NFS</span></span>
<span data-ttu-id="d0122-131">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="d0122-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="d0122-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0122-132">-ResourceGroupName</span></span>
<span data-ttu-id="d0122-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d0122-133">Resource Group Name</span></span>

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

### <span data-ttu-id="d0122-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="d0122-134">-SMB</span></span>
<span data-ttu-id="d0122-135">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="d0122-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="d0122-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="d0122-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="d0122-137">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="d0122-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0122-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="d0122-138">-UserAccessRight</span></span>
<span data-ttu-id="d0122-139">기존 사용자 이름과 함께 SMB 공유 유형에 액세스할 수 있는 액세스 권한을 제공합니다. 예: @(@{"Username"="user-name-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="d0122-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="d0122-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0122-140">-Confirm</span></span>
<span data-ttu-id="d0122-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0122-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0122-142">-WhatIf</span></span>
<span data-ttu-id="d0122-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0122-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0122-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0122-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0122-145">CommonParameters</span></span>
<span data-ttu-id="d0122-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0122-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0122-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0122-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0122-148">입력</span><span class="sxs-lookup"><span data-stu-id="d0122-148">INPUTS</span></span>

### <span data-ttu-id="d0122-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d0122-149">System.String</span></span>

## <span data-ttu-id="d0122-150">출력</span><span class="sxs-lookup"><span data-stu-id="d0122-150">OUTPUTS</span></span>

### <span data-ttu-id="d0122-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d0122-151">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="d0122-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0122-152">NOTES</span></span>

## <span data-ttu-id="d0122-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0122-153">RELATED LINKS</span></span>
