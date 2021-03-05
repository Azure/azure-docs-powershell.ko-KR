---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 8a4183c148eda0f5f560d24c2b5874ff5577e85e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968635"
---
# <span data-ttu-id="b4482-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b4482-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="b4482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4482-102">SYNOPSIS</span></span>
<span data-ttu-id="b4482-103">ANF(Azure NetApp Files) 백업에 대한 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4482-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="b4482-104">구문</span><span class="sxs-lookup"><span data-stu-id="b4482-104">SYNTAX</span></span>

### <span data-ttu-id="b4482-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b4482-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4482-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4482-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4482-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4482-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4482-108">설명</span><span class="sxs-lookup"><span data-stu-id="b4482-108">DESCRIPTION</span></span>
<span data-ttu-id="b4482-109">**Get-AzNetAppFilesBackup** cmdlet은 ANF 백업에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b4482-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="b4482-110">예제</span><span class="sxs-lookup"><span data-stu-id="b4482-110">EXAMPLES</span></span>

### <span data-ttu-id="b4482-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4482-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="b4482-112">이 명령은 "MyVolume"이라는 볼륨에서 "MyAnfAccount"라는 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b4482-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="b4482-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b4482-113">PARAMETERS</span></span>

### <span data-ttu-id="b4482-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b4482-114">-AccountName</span></span>
<span data-ttu-id="b4482-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="b4482-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="b4482-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4482-116">-DefaultProfile</span></span>
<span data-ttu-id="b4482-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4482-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4482-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b4482-118">-Name</span></span>
<span data-ttu-id="b4482-119">ANF 백업의 이름</span><span class="sxs-lookup"><span data-stu-id="b4482-119">The name of the ANF backup</span></span>

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

### <span data-ttu-id="b4482-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b4482-120">-PoolName</span></span>
<span data-ttu-id="b4482-121">ANF 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="b4482-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="b4482-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4482-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4482-123">ANF 계정의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="b4482-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b4482-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4482-124">-ResourceId</span></span>
<span data-ttu-id="b4482-125">ANF Backup의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b4482-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="b4482-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="b4482-126">-VolumeName</span></span>
<span data-ttu-id="b4482-127">ANF 볼륨의 이름</span><span class="sxs-lookup"><span data-stu-id="b4482-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="b4482-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="b4482-128">-VolumeObject</span></span>
<span data-ttu-id="b4482-129">반환할 백업이 포함된 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="b4482-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="b4482-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4482-130">CommonParameters</span></span>
<span data-ttu-id="b4482-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b4482-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4482-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4482-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4482-133">입력</span><span class="sxs-lookup"><span data-stu-id="b4482-133">INPUTS</span></span>

### <span data-ttu-id="b4482-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b4482-134">System.String</span></span>

### <span data-ttu-id="b4482-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4482-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b4482-136">출력</span><span class="sxs-lookup"><span data-stu-id="b4482-136">OUTPUTS</span></span>

### <span data-ttu-id="b4482-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="b4482-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="b4482-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b4482-138">NOTES</span></span>

## <span data-ttu-id="b4482-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4482-139">RELATED LINKS</span></span>
