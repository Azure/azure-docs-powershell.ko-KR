---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187289"
---
# <span data-ttu-id="b3a1b-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b3a1b-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="b3a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a1b-103">ANF(Azure NetApp Files) 백업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="b3a1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3a1b-104">SYNTAX</span></span>

### <span data-ttu-id="b3a1b-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b3a1b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3a1b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a1b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3a1b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a1b-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a1b-108">설명</span><span class="sxs-lookup"><span data-stu-id="b3a1b-108">DESCRIPTION</span></span>
<span data-ttu-id="b3a1b-109">**Get-AzNetAppFilesBackup** cmdlet은 ANF 백업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="b3a1b-110">예제</span><span class="sxs-lookup"><span data-stu-id="b3a1b-110">EXAMPLES</span></span>

### <span data-ttu-id="b3a1b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3a1b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="b3a1b-112">이 명령은 "MyVolume"이라는 볼륨에서 "MyAnfAccount"라는 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="b3a1b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3a1b-113">PARAMETERS</span></span>

### <span data-ttu-id="b3a1b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3a1b-114">-AccountName</span></span>
<span data-ttu-id="b3a1b-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="b3a1b-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="b3a1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a1b-116">-DefaultProfile</span></span>
<span data-ttu-id="b3a1b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a1b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b3a1b-118">-Name</span></span>
<span data-ttu-id="b3a1b-119">ANF 백업의 이름</span><span class="sxs-lookup"><span data-stu-id="b3a1b-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1b-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b3a1b-120">-PoolName</span></span>
<span data-ttu-id="b3a1b-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="b3a1b-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b3a1b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a1b-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3a1b-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="b3a1b-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b3a1b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a1b-124">-ResourceId</span></span>
<span data-ttu-id="b3a1b-125">ANF Backup의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b3a1b-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="b3a1b-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="b3a1b-126">-VolumeName</span></span>
<span data-ttu-id="b3a1b-127">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="b3a1b-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1b-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="b3a1b-128">-VolumeObject</span></span>
<span data-ttu-id="b3a1b-129">반환할 백업이 포함된 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="b3a1b-129">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a1b-130">CommonParameters</span></span>
<span data-ttu-id="b3a1b-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a1b-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3a1b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a1b-133">입력</span><span class="sxs-lookup"><span data-stu-id="b3a1b-133">INPUTS</span></span>

### <span data-ttu-id="b3a1b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b3a1b-134">System.String</span></span>

### <span data-ttu-id="b3a1b-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b3a1b-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b3a1b-136">출력</span><span class="sxs-lookup"><span data-stu-id="b3a1b-136">OUTPUTS</span></span>

### <span data-ttu-id="b3a1b-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b3a1b-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="b3a1b-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3a1b-138">NOTES</span></span>

## <span data-ttu-id="b3a1b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3a1b-139">RELATED LINKS</span></span>
