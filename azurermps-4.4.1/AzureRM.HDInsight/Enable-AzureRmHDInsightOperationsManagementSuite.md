---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703118"
---
# <span data-ttu-id="5b037-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="5b037-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="5b037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b037-102">SYNOPSIS</span></span>
<span data-ttu-id="5b037-103">HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하도록 설정 하 고, 사용 중에 지정 된 OMS 작업 영역으로 관련 로그를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b037-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5b037-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b037-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5b037-105">DESCRIPTION</span></span>
<span data-ttu-id="5b037-106">**AzureRmHDInsightOperationsManagementSuite** Cmdlet은 Azure HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5b037-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5b037-107">EXAMPLES</span></span>

### <span data-ttu-id="5b037-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b037-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="5b037-109">HDInsight 클러스터에서 OMS (Operations Management Suite)가 사용 하도록 설정 되 고 id 1d364e89-bb71-4503-aa3d-a23535aea7bd를 사용 하 여 관련 로그가 OMS 작업 영역으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="5b037-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b037-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="5b037-111">HDInsight 클러스터에서 OMS (Operations Management Suite)가 사용 하도록 설정 되 고 id 1d364e89-bb71-4503-aa3d-a23535aea7bd를 사용 하 여 관련 로그가 OMS 작업 영역으로 전송 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="5b037-112">변수</span><span class="sxs-lookup"><span data-stu-id="5b037-112">PARAMETERS</span></span>

### <span data-ttu-id="5b037-113">-이름</span><span class="sxs-lookup"><span data-stu-id="5b037-113">-Name</span></span>
<span data-ttu-id="5b037-114">OMS (Operations Management Suite)를 사용 하도록 설정할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b037-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5b037-115">-PrimaryKey</span></span>
<span data-ttu-id="5b037-116">OMS (Operations Management Suite) 작업 영역의 기본 키입니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b037-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b037-117">-ResourceGroupName</span></span>
<span data-ttu-id="5b037-118">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="5b037-119">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5b037-119">-WorkspaceId</span></span>
<span data-ttu-id="5b037-120">OMS (Operations Management Suite) 작업 영역의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b037-121">-확인</span><span class="sxs-lookup"><span data-stu-id="5b037-121">-Confirm</span></span>
<span data-ttu-id="5b037-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b037-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b037-123">-DefaultProfile</span></span>
<span data-ttu-id="5b037-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b037-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b037-125">-WhatIf</span></span>
<span data-ttu-id="5b037-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b037-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b037-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b037-128">CommonParameters</span></span>
<span data-ttu-id="5b037-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b037-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b037-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b037-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b037-131">입력</span><span class="sxs-lookup"><span data-stu-id="5b037-131">INPUTS</span></span>

### <span data-ttu-id="5b037-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b037-132">System.String</span></span>

## <span data-ttu-id="5b037-133">출력</span><span class="sxs-lookup"><span data-stu-id="5b037-133">OUTPUTS</span></span>

### <span data-ttu-id="5b037-134">Microsoft. Azure. 관리 리소스</span><span class="sxs-lookup"><span data-stu-id="5b037-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="5b037-135">상속자</span><span class="sxs-lookup"><span data-stu-id="5b037-135">NOTES</span></span>

## <span data-ttu-id="5b037-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b037-136">RELATED LINKS</span></span>

