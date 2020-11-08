---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204085"
---
# <span data-ttu-id="f0492-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f0492-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="f0492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0492-102">SYNOPSIS</span></span>
<span data-ttu-id="f0492-103">일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-103">Creates a Batch account.</span></span>

## <span data-ttu-id="f0492-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0492-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0492-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0492-105">DESCRIPTION</span></span>
<span data-ttu-id="f0492-106">**AzBatchAccount** cmdlet은 지정 된 리소스 그룹 및 위치에 대 한 Azure Batch 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="f0492-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f0492-107">EXAMPLES</span></span>

### <span data-ttu-id="f0492-108">예제 1: 일괄 처리 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="f0492-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="f0492-109">이 명령은 미국 내 위치에서 ResourceGroup03 리소스 그룹을 사용 하 여 pfuller 이라는 일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="f0492-110">변수</span><span class="sxs-lookup"><span data-stu-id="f0492-110">PARAMETERS</span></span>

### <span data-ttu-id="f0492-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0492-111">-AccountName</span></span>
<span data-ttu-id="f0492-112">이 cmdlet이 만드는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="f0492-113">일괄 처리 계정 이름은 3 ~ 24 자 사이 여야 하며 숫자와 소문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f0492-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="f0492-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0492-116">-DefaultProfile</span></span>
<span data-ttu-id="f0492-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0492-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f0492-118">-IdentityType</span></span>
<span data-ttu-id="f0492-119">BatchAccount와 연결 된 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-120">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="f0492-120">-KeyVaultId</span></span>
<span data-ttu-id="f0492-121">일괄 처리 계정과 연결 된 Azure 키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="f0492-122">-KeyVaultUrl</span></span>
<span data-ttu-id="f0492-123">일괄 처리 계정과 연결 된 Azure 키 보관소의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-123">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-124">-위치</span><span class="sxs-lookup"><span data-stu-id="f0492-124">-Location</span></span>
<span data-ttu-id="f0492-125">이 cmdlet이 계정을 만드는 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="f0492-126">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0492-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="f0492-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="f0492-127">-PoolAllocationMode</span></span>
<span data-ttu-id="f0492-128">Batch 계정에서 풀을 만들기 위한 배정 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-128">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f0492-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="f0492-130">공용 네트워크 액세스 형식</span><span class="sxs-lookup"><span data-stu-id="f0492-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0492-131">-ResourceGroupName</span></span>
<span data-ttu-id="f0492-132">이 cmdlet이 계정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="f0492-133">태그</span><span class="sxs-lookup"><span data-stu-id="f0492-133">-Tag</span></span>
<span data-ttu-id="f0492-134">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f0492-135">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f0492-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0492-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0492-136">CommonParameters</span></span>
<span data-ttu-id="f0492-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0492-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0492-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0492-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0492-139">입력</span><span class="sxs-lookup"><span data-stu-id="f0492-139">INPUTS</span></span>

### <span data-ttu-id="f0492-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0492-140">System.String</span></span>

### <span data-ttu-id="f0492-141">시스템. Null 허용 ' 1 [[Microsoft.Azure.Management.Batch. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 9.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f0492-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f0492-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f0492-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f0492-143">출력</span><span class="sxs-lookup"><span data-stu-id="f0492-143">OUTPUTS</span></span>

### <span data-ttu-id="f0492-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f0492-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f0492-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f0492-145">NOTES</span></span>

## <span data-ttu-id="f0492-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0492-146">RELATED LINKS</span></span>

[<span data-ttu-id="f0492-147">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f0492-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="f0492-148">제거-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f0492-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="f0492-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="f0492-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="f0492-150">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0492-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
