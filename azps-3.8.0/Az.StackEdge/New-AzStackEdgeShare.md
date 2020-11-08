---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043068"
---
# <span data-ttu-id="01341-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="01341-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="01341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01341-102">SYNOPSIS</span></span>
<span data-ttu-id="01341-103">장치에서 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01341-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="01341-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01341-104">SYNTAX</span></span>

### <span data-ttu-id="01341-105">SmbParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="01341-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01341-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="01341-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01341-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="01341-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01341-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="01341-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01341-109">설명은</span><span class="sxs-lookup"><span data-stu-id="01341-109">DESCRIPTION</span></span>
<span data-ttu-id="01341-110">**AzStackEdgeShare** Cmdlet은 스택 가장자리 장치에서 새 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01341-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="01341-111">예제의</span><span class="sxs-lookup"><span data-stu-id="01341-111">EXAMPLES</span></span>

### <span data-ttu-id="01341-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="01341-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="01341-113">변수</span><span class="sxs-lookup"><span data-stu-id="01341-113">PARAMETERS</span></span>

### <span data-ttu-id="01341-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01341-114">-AsJob</span></span>
<span data-ttu-id="01341-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="01341-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01341-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="01341-116">-ClientAccessRight</span></span>
<span data-ttu-id="01341-117">Ds (예: @ {"ClientId" = "192.168.10.10)에 대 한 읽기/쓰기 액세스 AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="01341-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="01341-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="01341-118">-CloudShare</span></span>
<span data-ttu-id="01341-119">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="01341-119">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="01341-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="01341-120">-ContainerName</span></span>
<span data-ttu-id="01341-121">컨테이너 이름 (지정 된 데이터 형식을 기반으로 하 여 Azure Files/Pageblob/Block blob의 이름을 나타냄)</span><span class="sxs-lookup"><span data-stu-id="01341-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

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

### <span data-ttu-id="01341-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="01341-122">-DataFormat</span></span>
<span data-ttu-id="01341-123">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="01341-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="01341-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01341-124">-DefaultProfile</span></span>
<span data-ttu-id="01341-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01341-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01341-126">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="01341-126">-DeviceName</span></span>
<span data-ttu-id="01341-127">장치 이름</span><span class="sxs-lookup"><span data-stu-id="01341-127">Device Name</span></span>

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

### <span data-ttu-id="01341-128">-이름</span><span class="sxs-lookup"><span data-stu-id="01341-128">-Name</span></span>
<span data-ttu-id="01341-129">자원 이름</span><span class="sxs-lookup"><span data-stu-id="01341-129">Resource Name</span></span>

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

### <span data-ttu-id="01341-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="01341-130">-NFS</span></span>
<span data-ttu-id="01341-131">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="01341-131">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="01341-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01341-132">-ResourceGroupName</span></span>
<span data-ttu-id="01341-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="01341-133">Resource Group Name</span></span>

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

### <span data-ttu-id="01341-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="01341-134">-SMB</span></span>
<span data-ttu-id="01341-135">공유를 만드는 경우 AccessProtocol</span><span class="sxs-lookup"><span data-stu-id="01341-135">AccessProtocol in the case of creating Share</span></span>

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

### <span data-ttu-id="01341-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="01341-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="01341-137">기존 StorageAccountCredential의 리소스 이름 제공</span><span class="sxs-lookup"><span data-stu-id="01341-137">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="01341-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="01341-138">-UserAccessRight</span></span>
<span data-ttu-id="01341-139">예: @ (@ {"Username" = "user-name-1")에 액세스할 수 있도록 기존 사용자 이름과 함께 액세스 권한을 제공 합니다. AccessRight "=" Read "}, @ {" Username "=" 사용자 이름-2 ";" AccessRight "=" Read "}, @ {" Username "=" 사용자 이름-3 ";" AccessRight "=" 사용자 지정 "})</span><span class="sxs-lookup"><span data-stu-id="01341-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="01341-140">-확인</span><span class="sxs-lookup"><span data-stu-id="01341-140">-Confirm</span></span>
<span data-ttu-id="01341-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01341-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01341-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01341-142">-WhatIf</span></span>
<span data-ttu-id="01341-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01341-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01341-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01341-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01341-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01341-145">CommonParameters</span></span>
<span data-ttu-id="01341-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01341-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01341-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="01341-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01341-148">입력</span><span class="sxs-lookup"><span data-stu-id="01341-148">INPUTS</span></span>

### <span data-ttu-id="01341-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01341-149">System.String</span></span>

## <span data-ttu-id="01341-150">출력</span><span class="sxs-lookup"><span data-stu-id="01341-150">OUTPUTS</span></span>

### <span data-ttu-id="01341-151">StackEdge. PSStackEdgeShare에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="01341-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="01341-152">상속자</span><span class="sxs-lookup"><span data-stu-id="01341-152">NOTES</span></span>

## <span data-ttu-id="01341-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01341-153">RELATED LINKS</span></span>
