---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870945"
---
# <span data-ttu-id="cae09-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cae09-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="cae09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cae09-102">SYNOPSIS</span></span>
<span data-ttu-id="cae09-103">ANF (Azure NetApp Files) 볼륨에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="cae09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cae09-104">SYNTAX</span></span>

### <span data-ttu-id="cae09-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cae09-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cae09-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae09-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cae09-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cae09-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cae09-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cae09-108">DESCRIPTION</span></span>
<span data-ttu-id="cae09-109">**AzNetAppFilesVolume** cmdlet은 anf 볼륨에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="cae09-110">예제의</span><span class="sxs-lookup"><span data-stu-id="cae09-110">EXAMPLES</span></span>

### <span data-ttu-id="cae09-111">예제 1: ANF 볼륨 가져오기</span><span class="sxs-lookup"><span data-stu-id="cae09-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="cae09-112">이 명령은 "MyAnfPool" 풀에서 MyAnfVolume 이라는 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="cae09-113">변수</span><span class="sxs-lookup"><span data-stu-id="cae09-113">PARAMETERS</span></span>

### <span data-ttu-id="cae09-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cae09-114">-AccountName</span></span>
<span data-ttu-id="cae09-115">ANF 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="cae09-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="cae09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae09-116">-DefaultProfile</span></span>
<span data-ttu-id="cae09-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae09-118">-이름</span><span class="sxs-lookup"><span data-stu-id="cae09-118">-Name</span></span>
<span data-ttu-id="cae09-119">ANF 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae09-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="cae09-120">-PoolName</span></span>
<span data-ttu-id="cae09-121">ANF 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="cae09-122">-Poo</span><span class="sxs-lookup"><span data-stu-id="cae09-122">-PoolObject</span></span>
<span data-ttu-id="cae09-123">반환할 볼륨을 포함 하는 pool 개체</span><span class="sxs-lookup"><span data-stu-id="cae09-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae09-124">-ResourceGroupName</span></span>
<span data-ttu-id="cae09-125">ANF 볼륨의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cae09-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="cae09-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cae09-126">-ResourceId</span></span>
<span data-ttu-id="cae09-127">ANF 볼륨의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="cae09-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="cae09-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae09-128">CommonParameters</span></span>
<span data-ttu-id="cae09-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cae09-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cae09-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cae09-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae09-131">입력</span><span class="sxs-lookup"><span data-stu-id="cae09-131">INPUTS</span></span>

### <span data-ttu-id="cae09-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cae09-132">System.String</span></span>

### <span data-ttu-id="cae09-133">Microsoft. p. p. p. p i p. p i a p. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="cae09-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="cae09-134">출력</span><span class="sxs-lookup"><span data-stu-id="cae09-134">OUTPUTS</span></span>

### <span data-ttu-id="cae09-135">Microsoft. Azure. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="cae09-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="cae09-136">상속자</span><span class="sxs-lookup"><span data-stu-id="cae09-136">NOTES</span></span>

## <span data-ttu-id="cae09-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cae09-137">RELATED LINKS</span></span>
