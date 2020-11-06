---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 2f051fb0724ac266753d87fc30489398a4aa64a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528378"
---
# <span data-ttu-id="a7784-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a7784-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="a7784-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7784-102">SYNOPSIS</span></span>
<span data-ttu-id="a7784-103">저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7784-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7784-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a7784-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7784-105">DESCRIPTION</span></span>
<span data-ttu-id="a7784-106">**AzureStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a7784-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7784-107">EXAMPLES</span></span>

### <span data-ttu-id="a7784-108">예제 1: azure 저장소 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="a7784-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="a7784-109">이 명령은 tableabc의 이름을 사용 하 여 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="a7784-110">예제 2: 여러 azure storage 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="a7784-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="a7784-111">이 명령은 여러 개의 표를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-111">This command creates multiple tables.</span></span>
<span data-ttu-id="a7784-112">.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a7784-113">변수</span><span class="sxs-lookup"><span data-stu-id="a7784-113">PARAMETERS</span></span>

### <span data-ttu-id="a7784-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a7784-114">-Context</span></span>
<span data-ttu-id="a7784-115">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-115">Specifies the storage context.</span></span>
<span data-ttu-id="a7784-116">이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7784-117">-이름</span><span class="sxs-lookup"><span data-stu-id="a7784-117">-Name</span></span>
<span data-ttu-id="a7784-118">새 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7784-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7784-119">CommonParameters</span></span>
<span data-ttu-id="a7784-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7784-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7784-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7784-122">입력</span><span class="sxs-lookup"><span data-stu-id="a7784-122">INPUTS</span></span>

### <span data-ttu-id="a7784-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7784-123">IStorageContext</span></span>

<span data-ttu-id="a7784-124">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a7784-125">이름</span><span class="sxs-lookup"><span data-stu-id="a7784-125">String</span></span>

<span data-ttu-id="a7784-126">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a7784-127">출력</span><span class="sxs-lookup"><span data-stu-id="a7784-127">OUTPUTS</span></span>

### <span data-ttu-id="a7784-128">WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7784-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="a7784-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a7784-129">NOTES</span></span>

## <span data-ttu-id="a7784-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7784-130">RELATED LINKS</span></span>

[<span data-ttu-id="a7784-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a7784-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="a7784-132">제거-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a7784-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


