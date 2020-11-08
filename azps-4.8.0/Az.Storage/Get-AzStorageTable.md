---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048595"
---
# <span data-ttu-id="c6c7e-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c7e-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="c6c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c7e-103">저장소 테이블을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-103">Lists the storage tables.</span></span>

## <span data-ttu-id="c6c7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6c7e-104">SYNTAX</span></span>

### <span data-ttu-id="c6c7e-105">TableName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6c7e-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6c7e-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="c6c7e-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6c7e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c6c7e-107">DESCRIPTION</span></span>
<span data-ttu-id="c6c7e-108">**AzStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c6c7e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c6c7e-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c7e-110">예제 1: 모든 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="c6c7e-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="c6c7e-111">이 명령은 저장소 계정에 대 한 모든 저장소 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="c6c7e-112">예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="c6c7e-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="c6c7e-113">이 명령은 와일드 카드 문자를 사용 하 여 이름이 table로 시작 하는 저장소 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="c6c7e-114">예제 3: 테이블 이름 접두사를 사용 하 여 Azure Storage 테이블 나열</span><span class="sxs-lookup"><span data-stu-id="c6c7e-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="c6c7e-115">이 명령은 *Prefix* 매개 변수를 사용 하 여 이름이 table로 시작 하는 저장소 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="c6c7e-116">변수</span><span class="sxs-lookup"><span data-stu-id="c6c7e-116">PARAMETERS</span></span>

### <span data-ttu-id="c6c7e-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c6c7e-117">-Context</span></span>
<span data-ttu-id="c6c7e-118">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-118">Specifies the storage context.</span></span>
<span data-ttu-id="c6c7e-119">이를 만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6c7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c7e-120">-DefaultProfile</span></span>
<span data-ttu-id="c6c7e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6c7e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c6c7e-122">-Name</span></span>
<span data-ttu-id="c6c7e-123">테이블 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-123">Specifies the table name.</span></span>
<span data-ttu-id="c6c7e-124">테이블 이름이 비어 있으면 cmdlet에 모든 테이블이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="c6c7e-125">그렇지 않으면 지정 된 이름 또는 일반 이름 패턴과 일치 하는 모든 테이블이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="c6c7e-126">-접두사</span><span class="sxs-lookup"><span data-stu-id="c6c7e-126">-Prefix</span></span>
<span data-ttu-id="c6c7e-127">가져오려는 테이블 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="c6c7e-128">이를 사용 하 여 같은 문자열로 시작 하는 테이블 등의 모든 테이블을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="c6c7e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c7e-129">CommonParameters</span></span>
<span data-ttu-id="c6c7e-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c7e-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c7e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c7e-132">입력</span><span class="sxs-lookup"><span data-stu-id="c6c7e-132">INPUTS</span></span>

### <span data-ttu-id="c6c7e-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6c7e-133">System.String</span></span>

### <span data-ttu-id="c6c7e-134">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6c7e-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6c7e-135">출력</span><span class="sxs-lookup"><span data-stu-id="c6c7e-135">OUTPUTS</span></span>

### <span data-ttu-id="c6c7e-136">WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6c7e-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="c6c7e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="c6c7e-137">NOTES</span></span>

## <span data-ttu-id="c6c7e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6c7e-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6c7e-139">새로운 AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c7e-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="c6c7e-140">제거-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c7e-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


