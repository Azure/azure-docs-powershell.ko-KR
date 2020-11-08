---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216347"
---
# <span data-ttu-id="4581e-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="4581e-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="4581e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4581e-102">SYNOPSIS</span></span>
<span data-ttu-id="4581e-103">저장소 계정의 개체 복제 정책을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="4581e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4581e-104">SYNTAX</span></span>

### <span data-ttu-id="4581e-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4581e-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4581e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4581e-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4581e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4581e-107">DESCRIPTION</span></span>
<span data-ttu-id="4581e-108">**Get-AzStorageObjectReplicationPolicy** Cmdlet은 저장소 계정의 개체 복제 정책을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="4581e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4581e-109">EXAMPLES</span></span>

### <span data-ttu-id="4581e-110">예제 1: 특정 정책 Id를 사용 하 여 개체 복제 정책을 가져오고 해당 규칙을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
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

<span data-ttu-id="4581e-111">이 명령은 특정 정책 Id를 사용 하 여 개체 복제 정책을 가져오고 해당 규칙을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="4581e-112">예제 2: 저장소 계정의 개체 복제 정책 목록 표시</span><span class="sxs-lookup"><span data-stu-id="4581e-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="4581e-113">이 명령은 저장소 계정에서 개체 복제 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="4581e-114">변수</span><span class="sxs-lookup"><span data-stu-id="4581e-114">PARAMETERS</span></span>

### <span data-ttu-id="4581e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4581e-115">-DefaultProfile</span></span>
<span data-ttu-id="4581e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4581e-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="4581e-117">-PolicyId</span></span>
<span data-ttu-id="4581e-118">개체 복제 정책 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-118">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="4581e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4581e-119">-ResourceGroupName</span></span>
<span data-ttu-id="4581e-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="4581e-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4581e-121">-StorageAccount</span></span>
<span data-ttu-id="4581e-122">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="4581e-122">Storage account object</span></span>

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

### <span data-ttu-id="4581e-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4581e-123">-StorageAccountName</span></span>
<span data-ttu-id="4581e-124">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="4581e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4581e-125">CommonParameters</span></span>
<span data-ttu-id="4581e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4581e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4581e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4581e-128">입력</span><span class="sxs-lookup"><span data-stu-id="4581e-128">INPUTS</span></span>

### <span data-ttu-id="4581e-129">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4581e-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4581e-130">출력</span><span class="sxs-lookup"><span data-stu-id="4581e-130">OUTPUTS</span></span>

### <span data-ttu-id="4581e-131">PSObjectReplicationPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="4581e-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="4581e-132">상속자</span><span class="sxs-lookup"><span data-stu-id="4581e-132">NOTES</span></span>

## <span data-ttu-id="4581e-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4581e-133">RELATED LINKS</span></span>
