---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880242"
---
# <span data-ttu-id="aa123-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="aa123-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="aa123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa123-102">SYNOPSIS</span></span>
<span data-ttu-id="aa123-103">일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-103">Creates a Batch account.</span></span>

## <span data-ttu-id="aa123-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa123-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa123-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aa123-105">DESCRIPTION</span></span>
<span data-ttu-id="aa123-106">**AzBatchAccount** cmdlet은 지정 된 리소스 그룹 및 위치에 대 한 Azure Batch 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="aa123-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aa123-107">EXAMPLES</span></span>

### <span data-ttu-id="aa123-108">예제 1: 일괄 처리 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="aa123-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="aa123-109">이 명령은 미국 내 위치에서 ResourceGroup03 리소스 그룹을 사용 하 여 pfuller 이라는 일괄 처리 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="aa123-110">변수</span><span class="sxs-lookup"><span data-stu-id="aa123-110">PARAMETERS</span></span>

### <span data-ttu-id="aa123-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aa123-111">-AccountName</span></span>
<span data-ttu-id="aa123-112">이 cmdlet이 만드는 일괄 처리 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="aa123-113">일괄 처리 계정 이름은 3 ~ 24 자 사이 여야 하며 숫자와 소문자만 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="aa123-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="aa123-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="aa123-115">자동 저장소에 사용 되는 저장소 계정의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="aa123-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa123-116">-DefaultProfile</span></span>
<span data-ttu-id="aa123-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa123-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="aa123-118">-KeyVaultId</span></span>
<span data-ttu-id="aa123-119">일괄 처리 계정과 연결 된 Azure 키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="aa123-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="aa123-120">-KeyVaultUrl</span></span>
<span data-ttu-id="aa123-121">일괄 처리 계정과 연결 된 Azure 키 보관소의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="aa123-122">-위치</span><span class="sxs-lookup"><span data-stu-id="aa123-122">-Location</span></span>
<span data-ttu-id="aa123-123">이 cmdlet이 계정을 만드는 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="aa123-124">자세한 내용은 [Azure 지역을](https://azure.microsoft.com/en-us/regions)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa123-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="aa123-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="aa123-125">-PoolAllocationMode</span></span>
<span data-ttu-id="aa123-126">Batch 계정에서 풀을 만들기 위한 배정 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-126">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="aa123-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa123-127">-ResourceGroupName</span></span>
<span data-ttu-id="aa123-128">이 cmdlet이 계정을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="aa123-129">태그</span><span class="sxs-lookup"><span data-stu-id="aa123-129">-Tag</span></span>
<span data-ttu-id="aa123-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa123-131">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="aa123-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa123-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa123-132">CommonParameters</span></span>
<span data-ttu-id="aa123-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa123-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa123-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa123-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa123-135">입력</span><span class="sxs-lookup"><span data-stu-id="aa123-135">INPUTS</span></span>

### <span data-ttu-id="aa123-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa123-136">System.String</span></span>

### <span data-ttu-id="aa123-137">시스템. Null 허용 ' 1 [[Microsoft.Azure.Management.Batch. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aa123-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aa123-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="aa123-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aa123-139">출력</span><span class="sxs-lookup"><span data-stu-id="aa123-139">OUTPUTS</span></span>

### <span data-ttu-id="aa123-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="aa123-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="aa123-141">상속자</span><span class="sxs-lookup"><span data-stu-id="aa123-141">NOTES</span></span>

## <span data-ttu-id="aa123-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa123-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa123-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="aa123-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="aa123-144">제거-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="aa123-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="aa123-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="aa123-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="aa123-146">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aa123-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
