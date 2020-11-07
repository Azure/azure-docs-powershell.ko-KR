---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700779"
---
# <span data-ttu-id="95f7c-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="95f7c-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="95f7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="95f7c-103">ANF (Azure NetApp Files) 스냅숏의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="95f7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95f7c-104">SYNTAX</span></span>

### <span data-ttu-id="95f7c-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="95f7c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95f7c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95f7c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95f7c-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95f7c-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f7c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="95f7c-108">DESCRIPTION</span></span>
<span data-ttu-id="95f7c-109">**Get-AzNetAppFilesSnapshot** cmdlet은 anf 스냅숏의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="95f7c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="95f7c-110">EXAMPLES</span></span>

### <span data-ttu-id="95f7c-111">예제 1: ANF 스냅숏 가져오기</span><span class="sxs-lookup"><span data-stu-id="95f7c-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="95f7c-112">이 명령은 "MyAnfVolume" 볼륨에서 MyAnfSnapshot 라는 스냅샷을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="95f7c-113">변수</span><span class="sxs-lookup"><span data-stu-id="95f7c-113">PARAMETERS</span></span>

### <span data-ttu-id="95f7c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95f7c-114">-AccountName</span></span>
<span data-ttu-id="95f7c-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="95f7c-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f7c-116">-DefaultProfile</span></span>
<span data-ttu-id="95f7c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="95f7c-118">-Name</span></span>
<span data-ttu-id="95f7c-119">ANF 스냅숏의 이름</span><span class="sxs-lookup"><span data-stu-id="95f7c-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="95f7c-120">-PoolName</span></span>
<span data-ttu-id="95f7c-121">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f7c-122">-ResourceGroupName</span></span>
<span data-ttu-id="95f7c-123">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="95f7c-123">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95f7c-124">-ResourceId</span></span>
<span data-ttu-id="95f7c-125">ANF 스냅숏의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="95f7c-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="95f7c-126">-VolumeName</span></span>
<span data-ttu-id="95f7c-127">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-127">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="95f7c-128">-VolumeObject</span></span>
<span data-ttu-id="95f7c-129">반환할 스냅숏을 포함 하는 볼륨 개체</span><span class="sxs-lookup"><span data-stu-id="95f7c-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95f7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f7c-130">CommonParameters</span></span>
<span data-ttu-id="95f7c-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95f7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="95f7c-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f7c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f7c-133">입력</span><span class="sxs-lookup"><span data-stu-id="95f7c-133">INPUTS</span></span>

### <span data-ttu-id="95f7c-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95f7c-134">System.String</span></span>

### <span data-ttu-id="95f7c-135">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="95f7c-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="95f7c-136">출력</span><span class="sxs-lookup"><span data-stu-id="95f7c-136">OUTPUTS</span></span>

### <span data-ttu-id="95f7c-137">PSNetAppFilesSnapshot-. p m.</span><span class="sxs-lookup"><span data-stu-id="95f7c-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="95f7c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="95f7c-138">NOTES</span></span>

## <span data-ttu-id="95f7c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95f7c-139">RELATED LINKS</span></span>
