---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: b65bfc61b354a5a45ac009b40b54de46d94ef56c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490011"
---
# <span data-ttu-id="5b7c8-101">Get-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="5b7c8-101">Get-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="5b7c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b7c8-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7c8-103">ANF(Azure NetApp Files) 스냅숏 정책에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-103">Gets details of an Azure NetApp Files (ANF) snapshot policy.</span></span>

## <span data-ttu-id="5b7c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b7c8-104">SYNTAX</span></span>

### <span data-ttu-id="5b7c8-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b7c8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7c8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b7c8-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b7c8-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b7c8-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshotPolicy -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b7c8-108">설명</span><span class="sxs-lookup"><span data-stu-id="5b7c8-108">DESCRIPTION</span></span>
<span data-ttu-id="5b7c8-109">**Get-AzNetAppFilesSnapshotPolicy** cmdlet은 ANF 스냅숏 정책의 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-109">The **Get-AzNetAppFilesSnapshotPolicy** cmdlet gets details of an ANF snapshot policy.</span></span>

## <span data-ttu-id="5b7c8-110">예제</span><span class="sxs-lookup"><span data-stu-id="5b7c8-110">EXAMPLES</span></span>

### <span data-ttu-id="5b7c8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b7c8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MySnapshotPolicy"
```

<span data-ttu-id="5b7c8-112">이 명령은 "MyAnfAccount" 계정에 대해 "MyBackupPolicy"라는 백업 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="5b7c8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b7c8-113">PARAMETERS</span></span>

### <span data-ttu-id="5b7c8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5b7c8-114">-AccountName</span></span>
<span data-ttu-id="5b7c8-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="5b7c8-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="5b7c8-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5b7c8-116">-AccountObject</span></span>
<span data-ttu-id="5b7c8-117">새 스냅숏 정책 개체의 계정</span><span class="sxs-lookup"><span data-stu-id="5b7c8-117">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="5b7c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7c8-118">-DefaultProfile</span></span>
<span data-ttu-id="5b7c8-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b7c8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b7c8-120">-Name</span></span>
<span data-ttu-id="5b7c8-121">ANF 스냅숏 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="5b7c8-121">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b7c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b7c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b7c8-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="5b7c8-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5b7c8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b7c8-124">-ResourceId</span></span>
<span data-ttu-id="5b7c8-125">ANF 스냅숏 정책의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5b7c8-125">The resource id of the ANF Snapshot Policy</span></span>

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

### <span data-ttu-id="5b7c8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b7c8-126">-Confirm</span></span>
<span data-ttu-id="5b7c8-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7c8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7c8-128">-WhatIf</span></span>
<span data-ttu-id="5b7c8-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b7c8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b7c8-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b7c8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7c8-131">CommonParameters</span></span>
<span data-ttu-id="5b7c8-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7c8-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b7c8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7c8-134">입력</span><span class="sxs-lookup"><span data-stu-id="5b7c8-134">INPUTS</span></span>

### <span data-ttu-id="5b7c8-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5b7c8-135">System.String</span></span>

### <span data-ttu-id="5b7c8-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5b7c8-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5b7c8-137">출력</span><span class="sxs-lookup"><span data-stu-id="5b7c8-137">OUTPUTS</span></span>

### <span data-ttu-id="5b7c8-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="5b7c8-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="5b7c8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b7c8-139">NOTES</span></span>

## <span data-ttu-id="5b7c8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b7c8-140">RELATED LINKS</span></span>
