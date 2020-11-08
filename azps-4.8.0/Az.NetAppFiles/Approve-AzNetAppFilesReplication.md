---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213469"
---
# <span data-ttu-id="147bc-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="147bc-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="147bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="147bc-102">SYNOPSIS</span></span>
<span data-ttu-id="147bc-103">원본 볼륨에서 복제 연결 승인/권한 부여</span><span class="sxs-lookup"><span data-stu-id="147bc-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="147bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="147bc-104">SYNTAX</span></span>

### <span data-ttu-id="147bc-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="147bc-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="147bc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="147bc-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="147bc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="147bc-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="147bc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="147bc-108">DESCRIPTION</span></span>
<span data-ttu-id="147bc-109">원본 볼륨에서 복제 연결 승인</span><span class="sxs-lookup"><span data-stu-id="147bc-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="147bc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="147bc-110">EXAMPLES</span></span>

### <span data-ttu-id="147bc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="147bc-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="147bc-112">이 명령은 MyAnfVolume에서 복제를 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="147bc-113">변수</span><span class="sxs-lookup"><span data-stu-id="147bc-113">PARAMETERS</span></span>

### <span data-ttu-id="147bc-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="147bc-114">-AccountName</span></span>
<span data-ttu-id="147bc-115">복제 원본 볼륨의 ANF 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="147bc-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="147bc-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="147bc-117">대상 데이터 보호 볼륨의 파일 시스템 id</span><span class="sxs-lookup"><span data-stu-id="147bc-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="147bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147bc-118">-DefaultProfile</span></span>
<span data-ttu-id="147bc-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="147bc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="147bc-120">-InputObject</span></span>
<span data-ttu-id="147bc-121">복제 대상을 승인 하는 ANF 원본 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="147bc-121">The ANF source volume object to authorized the replication destination</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="147bc-122">-이름</span><span class="sxs-lookup"><span data-stu-id="147bc-122">-Name</span></span>
<span data-ttu-id="147bc-123">ANF 복제 원본 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-123">The name of the ANF replication source volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="147bc-124">-PassThru</span></span>
<span data-ttu-id="147bc-125">지정 된 볼륨의 복제 권한을 수행할지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="147bc-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="147bc-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="147bc-126">-PoolName</span></span>
<span data-ttu-id="147bc-127">복제 원본 볼륨의 ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="147bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="147bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="147bc-129">ANF 복제 원본 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="147bc-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="147bc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="147bc-130">-ResourceId</span></span>
<span data-ttu-id="147bc-131">ANF 복제 원본 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="147bc-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="147bc-132">-확인</span><span class="sxs-lookup"><span data-stu-id="147bc-132">-Confirm</span></span>
<span data-ttu-id="147bc-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="147bc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147bc-134">-WhatIf</span></span>
<span data-ttu-id="147bc-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147bc-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="147bc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147bc-137">CommonParameters</span></span>
<span data-ttu-id="147bc-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="147bc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147bc-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="147bc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147bc-140">입력</span><span class="sxs-lookup"><span data-stu-id="147bc-140">INPUTS</span></span>

### <span data-ttu-id="147bc-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="147bc-141">System.String</span></span>

### <span data-ttu-id="147bc-142">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="147bc-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="147bc-143">출력</span><span class="sxs-lookup"><span data-stu-id="147bc-143">OUTPUTS</span></span>

### <span data-ttu-id="147bc-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="147bc-144">System.Boolean</span></span>

## <span data-ttu-id="147bc-145">상속자</span><span class="sxs-lookup"><span data-stu-id="147bc-145">NOTES</span></span>

## <span data-ttu-id="147bc-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="147bc-146">RELATED LINKS</span></span>
