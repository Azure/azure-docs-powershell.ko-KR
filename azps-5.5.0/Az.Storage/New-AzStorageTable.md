---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195729"
---
# <span data-ttu-id="e98ea-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e98ea-101">New-AzStorageTable</span></span>

## <span data-ttu-id="e98ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e98ea-103">저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-103">Creates a storage table.</span></span>

## <span data-ttu-id="e98ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="e98ea-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e98ea-105">설명</span><span class="sxs-lookup"><span data-stu-id="e98ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e98ea-106">**New-AzStorageTable** cmdlet은 Azure의 저장소 계정과 연결된 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="e98ea-107">예제</span><span class="sxs-lookup"><span data-stu-id="e98ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e98ea-108">예제 1: Azure Storage 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="e98ea-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="e98ea-109">이 명령은 tableabc 이름으로 저장소 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="e98ea-110">예제 2: 여러 Azure 저장소 테이블 만들기</span><span class="sxs-lookup"><span data-stu-id="e98ea-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="e98ea-111">이 명령은 여러 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-111">This command creates multiple tables.</span></span>
<span data-ttu-id="e98ea-112">.NET **문자열** 클래스의 Split  메서드를 사용하여 파이프라인에 이름을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="e98ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98ea-113">PARAMETERS</span></span>

### <span data-ttu-id="e98ea-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e98ea-114">-Context</span></span>
<span data-ttu-id="e98ea-115">저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-115">Specifies the storage context.</span></span>
<span data-ttu-id="e98ea-116">이 cmdlet을 만들 때 New-AzStorageContext 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e98ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98ea-117">-DefaultProfile</span></span>
<span data-ttu-id="e98ea-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e98ea-119">-Name</span></span>
<span data-ttu-id="e98ea-120">새 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="e98ea-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98ea-121">CommonParameters</span></span>
<span data-ttu-id="e98ea-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e98ea-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98ea-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e98ea-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98ea-124">입력</span><span class="sxs-lookup"><span data-stu-id="e98ea-124">INPUTS</span></span>

### <span data-ttu-id="e98ea-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e98ea-125">System.String</span></span>

### <span data-ttu-id="e98ea-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e98ea-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e98ea-127">출력</span><span class="sxs-lookup"><span data-stu-id="e98ea-127">OUTPUTS</span></span>

### <span data-ttu-id="e98ea-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="e98ea-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="e98ea-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e98ea-129">NOTES</span></span>

## <span data-ttu-id="e98ea-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e98ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="e98ea-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e98ea-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="e98ea-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="e98ea-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


