---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 14f42ae951fe25f7594eb6e314ac65bb678e29c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526440"
---
# <span data-ttu-id="d314e-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d314e-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="d314e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d314e-102">SYNOPSIS</span></span>
<span data-ttu-id="d314e-103">저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d314e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d314e-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d314e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d314e-105">DESCRIPTION</span></span>
<span data-ttu-id="d314e-106">**AzureStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d314e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d314e-107">EXAMPLES</span></span>

### <span data-ttu-id="d314e-108">예제 1: azure 저장소 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="d314e-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="d314e-109">이 명령은 tableabc의 이름을 사용 하 여 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="d314e-110">예제 2: 여러 azure storage 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="d314e-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="d314e-111">이 명령은 여러 개의 표를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-111">This command creates multiple tables.</span></span>
<span data-ttu-id="d314e-112">.NET **문자열** 클래스의 **Split** 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d314e-113">변수</span><span class="sxs-lookup"><span data-stu-id="d314e-113">PARAMETERS</span></span>

### <span data-ttu-id="d314e-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d314e-114">-Context</span></span>
<span data-ttu-id="d314e-115">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-115">Specifies the storage context.</span></span>
<span data-ttu-id="d314e-116">이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d314e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d314e-117">-DefaultProfile</span></span>
<span data-ttu-id="d314e-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d314e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d314e-119">-Name</span></span>
<span data-ttu-id="d314e-120">새 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d314e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d314e-121">CommonParameters</span></span>
<span data-ttu-id="d314e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d314e-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d314e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d314e-124">입력</span><span class="sxs-lookup"><span data-stu-id="d314e-124">INPUTS</span></span>

### <span data-ttu-id="d314e-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d314e-125">System.String</span></span>

### <span data-ttu-id="d314e-126">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d314e-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d314e-127">출력</span><span class="sxs-lookup"><span data-stu-id="d314e-127">OUTPUTS</span></span>

### <span data-ttu-id="d314e-128">WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d314e-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="d314e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d314e-129">NOTES</span></span>

## <span data-ttu-id="d314e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d314e-130">RELATED LINKS</span></span>

[<span data-ttu-id="d314e-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d314e-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="d314e-132">제거-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d314e-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


