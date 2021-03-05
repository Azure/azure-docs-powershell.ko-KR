---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 00d88c594d1f36c01bb47e7b392dcdd2ebeb2774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981483"
---
# <span data-ttu-id="2fbc8-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="2fbc8-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="2fbc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fbc8-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbc8-103">Storage 계정의 개체 복제 정책을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="2fbc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="2fbc8-104">SYNTAX</span></span>

### <span data-ttu-id="2fbc8-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2fbc8-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fbc8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2fbc8-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fbc8-107">설명</span><span class="sxs-lookup"><span data-stu-id="2fbc8-107">DESCRIPTION</span></span>
<span data-ttu-id="2fbc8-108">**Get-AzStorageObjectReplicationPolicy** cmdlet은 Storage 계정의 개체 복제 정책을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="2fbc8-109">예제</span><span class="sxs-lookup"><span data-stu-id="2fbc8-109">EXAMPLES</span></span>

### <span data-ttu-id="2fbc8-110">예제 1: 특정 정책 ID가 있는 개체 복제 정책을 구하고 해당 규칙을 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="2fbc8-111">이 명령은 특정 정책 ID가 있는 개체 복제 정책을 얻게 하여 해당 규칙을 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="2fbc8-112">예제 2:Storage 계정의 개체 복제 정책 나열</span><span class="sxs-lookup"><span data-stu-id="2fbc8-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="2fbc8-113">이 명령은 Storage 계정의 개체 복제 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="2fbc8-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2fbc8-114">PARAMETERS</span></span>

### <span data-ttu-id="2fbc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbc8-115">-DefaultProfile</span></span>
<span data-ttu-id="2fbc8-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fbc8-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="2fbc8-117">-PolicyId</span></span>
<span data-ttu-id="2fbc8-118">개체 복제 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbc8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbc8-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fbc8-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbc8-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fbc8-121">-StorageAccount</span></span>
<span data-ttu-id="2fbc8-122">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="2fbc8-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fbc8-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2fbc8-123">-StorageAccountName</span></span>
<span data-ttu-id="2fbc8-124">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fbc8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbc8-125">CommonParameters</span></span>
<span data-ttu-id="2fbc8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbc8-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2fbc8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbc8-128">입력</span><span class="sxs-lookup"><span data-stu-id="2fbc8-128">INPUTS</span></span>

### <span data-ttu-id="2fbc8-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fbc8-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2fbc8-130">출력</span><span class="sxs-lookup"><span data-stu-id="2fbc8-130">OUTPUTS</span></span>

### <span data-ttu-id="2fbc8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="2fbc8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="2fbc8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2fbc8-132">NOTES</span></span>

## <span data-ttu-id="2fbc8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fbc8-133">RELATED LINKS</span></span>
