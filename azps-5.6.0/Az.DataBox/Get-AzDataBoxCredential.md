---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: f5f811b28b349c6dbc9972c9a464a56a002b99f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998699"
---
# <span data-ttu-id="3c4ea-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="3c4ea-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="3c4ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4ea-103">특정 작업의 데이터 상자 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="3c4ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c4ea-104">SYNTAX</span></span>

### <span data-ttu-id="3c4ea-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c4ea-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c4ea-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c4ea-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c4ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="3c4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="3c4ea-108">**Get-AzDataBoxCredential** cmdlet은 특정 작업의 데이터 상자의 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="3c4ea-109">반환된 자격 증명 개체의 내부 속성은 다른 Sku 유형에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="3c4ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="3c4ea-110">EXAMPLES</span></span>

### <span data-ttu-id="3c4ea-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c4ea-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="3c4ea-112">지정된 작업의 JobSecrets를 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="3c4ea-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3c4ea-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="3c4ea-114">지정된 작업의 JobSecrets를 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="3c4ea-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c4ea-115">PARAMETERS</span></span>

### <span data-ttu-id="3c4ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4ea-116">-DefaultProfile</span></span>
<span data-ttu-id="3c4ea-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c4ea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3c4ea-118">-Name</span></span>
<span data-ttu-id="3c4ea-119">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="3c4ea-119">Databox Job Name</span></span>

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

### <span data-ttu-id="3c4ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c4ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="3c4ea-121">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3c4ea-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="3c4ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c4ea-122">-ResourceId</span></span>
<span data-ttu-id="3c4ea-123">Databox 작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="3c4ea-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="3c4ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4ea-124">CommonParameters</span></span>
<span data-ttu-id="3c4ea-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c4ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4ea-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c4ea-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4ea-127">입력</span><span class="sxs-lookup"><span data-stu-id="3c4ea-127">INPUTS</span></span>

### <span data-ttu-id="3c4ea-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3c4ea-128">System.String</span></span>

## <span data-ttu-id="3c4ea-129">출력</span><span class="sxs-lookup"><span data-stu-id="3c4ea-129">OUTPUTS</span></span>

### <span data-ttu-id="3c4ea-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3c4ea-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3c4ea-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c4ea-131">NOTES</span></span>

## <span data-ttu-id="3c4ea-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c4ea-132">RELATED LINKS</span></span>
