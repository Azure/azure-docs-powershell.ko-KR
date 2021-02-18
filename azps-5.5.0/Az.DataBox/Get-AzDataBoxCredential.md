---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181137"
---
# <span data-ttu-id="b37cf-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="b37cf-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="b37cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b37cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b37cf-103">특정 작업의 데이터 상자 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="b37cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="b37cf-104">SYNTAX</span></span>

### <span data-ttu-id="b37cf-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b37cf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b37cf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b37cf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b37cf-107">설명</span><span class="sxs-lookup"><span data-stu-id="b37cf-107">DESCRIPTION</span></span>
<span data-ttu-id="b37cf-108">**Get-AzDataBoxCredential** cmdlet은 특정 작업의 데이터 상자 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="b37cf-109">반환된 자격 증명 개체의 내부 속성은 SKU 유형마다 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="b37cf-110">예제</span><span class="sxs-lookup"><span data-stu-id="b37cf-110">EXAMPLES</span></span>

### <span data-ttu-id="b37cf-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b37cf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b37cf-112">지정된 작업의 JobSecrets를 다시 컴투스합니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="b37cf-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b37cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="b37cf-114">지정된 작업의 JobSecrets를 다시 컴투스합니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="b37cf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b37cf-115">PARAMETERS</span></span>

### <span data-ttu-id="b37cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37cf-116">-DefaultProfile</span></span>
<span data-ttu-id="b37cf-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b37cf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b37cf-118">-Name</span></span>
<span data-ttu-id="b37cf-119">Databox 작업 이름</span><span class="sxs-lookup"><span data-stu-id="b37cf-119">Databox Job Name</span></span>

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

### <span data-ttu-id="b37cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b37cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="b37cf-121">Databox 작업 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b37cf-121">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="b37cf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b37cf-122">-ResourceId</span></span>
<span data-ttu-id="b37cf-123">Databox 작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b37cf-123">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="b37cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37cf-124">CommonParameters</span></span>
<span data-ttu-id="b37cf-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b37cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37cf-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b37cf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37cf-127">입력</span><span class="sxs-lookup"><span data-stu-id="b37cf-127">INPUTS</span></span>

### <span data-ttu-id="b37cf-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b37cf-128">System.String</span></span>

## <span data-ttu-id="b37cf-129">출력</span><span class="sxs-lookup"><span data-stu-id="b37cf-129">OUTPUTS</span></span>

### <span data-ttu-id="b37cf-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b37cf-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b37cf-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b37cf-131">NOTES</span></span>

## <span data-ttu-id="b37cf-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b37cf-132">RELATED LINKS</span></span>
