---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195793"
---
# <span data-ttu-id="1d24b-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="1d24b-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="1d24b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d24b-102">SYNOPSIS</span></span>
<span data-ttu-id="1d24b-103">저장소 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-103">Lists the storage tables.</span></span>

## <span data-ttu-id="1d24b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d24b-104">SYNTAX</span></span>

### <span data-ttu-id="1d24b-105">TableName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d24b-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d24b-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="1d24b-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d24b-107">설명</span><span class="sxs-lookup"><span data-stu-id="1d24b-107">DESCRIPTION</span></span>
<span data-ttu-id="1d24b-108">**Get-AzStorageTable** cmdlet은 Azure의 저장소 계정과 연결된 저장소 테이블을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="1d24b-109">예제</span><span class="sxs-lookup"><span data-stu-id="1d24b-109">EXAMPLES</span></span>

### <span data-ttu-id="1d24b-110">예제 1: 모든 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="1d24b-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="1d24b-111">이 명령은 Storage 계정에 대한 모든 저장소 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="1d24b-112">예제 2: 와일드카드 문자를 사용하여 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="1d24b-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="1d24b-113">이 명령은 와일드카드 문자를 사용하여 이름이 테이블로 시작하는 저장소 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="1d24b-114">예제 3: 테이블 이름 사전을 사용하여 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="1d24b-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="1d24b-115">이 명령은 *Prefix* 매개 변수를 사용하여 이름이 테이블로 시작하는 저장소 테이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="1d24b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d24b-116">PARAMETERS</span></span>

### <span data-ttu-id="1d24b-117">-Context</span><span class="sxs-lookup"><span data-stu-id="1d24b-117">-Context</span></span>
<span data-ttu-id="1d24b-118">저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-118">Specifies the storage context.</span></span>
<span data-ttu-id="1d24b-119">이 cmdlet을 만들 때 New-AzStorageContext 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d24b-120">-DefaultProfile</span></span>
<span data-ttu-id="1d24b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d24b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1d24b-122">-Name</span></span>
<span data-ttu-id="1d24b-123">테이블 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-123">Specifies the table name.</span></span>
<span data-ttu-id="1d24b-124">테이블 이름이 비어 있는 경우 cmdlet에는 모든 테이블이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="1d24b-125">그렇지 않으면 지정된 이름 또는 일반 이름 패턴과 일치하는 모든 테이블이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24b-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1d24b-126">-Prefix</span></span>
<span data-ttu-id="1d24b-127">사용하려는 테이블 또는 테이블의 이름에 사용되는 prefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="1d24b-128">이를 사용하여 동일한 문자열로 시작하는 모든 테이블(예: 테이블)을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d24b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d24b-129">CommonParameters</span></span>
<span data-ttu-id="1d24b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d24b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d24b-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1d24b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d24b-132">입력</span><span class="sxs-lookup"><span data-stu-id="1d24b-132">INPUTS</span></span>

### <span data-ttu-id="1d24b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1d24b-133">System.String</span></span>

### <span data-ttu-id="1d24b-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1d24b-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1d24b-135">출력</span><span class="sxs-lookup"><span data-stu-id="1d24b-135">OUTPUTS</span></span>

### <span data-ttu-id="1d24b-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1d24b-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="1d24b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d24b-137">NOTES</span></span>

## <span data-ttu-id="1d24b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d24b-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d24b-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="1d24b-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="1d24b-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="1d24b-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


