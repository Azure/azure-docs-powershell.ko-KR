---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056449"
---
# <span data-ttu-id="f1657-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="f1657-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="f1657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1657-102">SYNOPSIS</span></span>
<span data-ttu-id="f1657-103">특정 작업의 databox 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1657-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="f1657-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1657-104">SYNTAX</span></span>

### <span data-ttu-id="f1657-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1657-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1657-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1657-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1657-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f1657-107">DESCRIPTION</span></span>
<span data-ttu-id="f1657-108">**AzDataBoxCredential** cmdlet은 특정 작업의 databox 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1657-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="f1657-109">반환 된 자격 증명 개체의 내부 속성은 Sku 형식에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="f1657-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="f1657-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f1657-110">EXAMPLES</span></span>

### <span data-ttu-id="f1657-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1657-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="f1657-112">지정 된 작업의 JobSecrets을 retuns.</span><span class="sxs-lookup"><span data-stu-id="f1657-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="f1657-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1657-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="f1657-114">지정 된 작업의 JobSecrets을 retuns.</span><span class="sxs-lookup"><span data-stu-id="f1657-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="f1657-115">변수</span><span class="sxs-lookup"><span data-stu-id="f1657-115">PARAMETERS</span></span>

### <span data-ttu-id="f1657-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1657-116">-DefaultProfile</span></span>
<span data-ttu-id="f1657-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1657-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1657-118">-이름</span><span class="sxs-lookup"><span data-stu-id="f1657-118">-Name</span></span>
<span data-ttu-id="f1657-119">Databox Job 이름</span><span class="sxs-lookup"><span data-stu-id="f1657-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1657-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1657-121">Databox Job 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f1657-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1657-122">-ResourceId</span></span>
<span data-ttu-id="f1657-123">Databox Job 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="f1657-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1657-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1657-124">CommonParameters</span></span>
<span data-ttu-id="f1657-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1657-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1657-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f1657-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1657-127">입력</span><span class="sxs-lookup"><span data-stu-id="f1657-127">INPUTS</span></span>

### <span data-ttu-id="f1657-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f1657-128">System.String</span></span>

## <span data-ttu-id="f1657-129">출력</span><span class="sxs-lookup"><span data-stu-id="f1657-129">OUTPUTS</span></span>

### <span data-ttu-id="f1657-130">DataBox, DataBox, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35])). t e 1. a n a. [[Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f1657-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f1657-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f1657-131">NOTES</span></span>

## <span data-ttu-id="f1657-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1657-132">RELATED LINKS</span></span>
