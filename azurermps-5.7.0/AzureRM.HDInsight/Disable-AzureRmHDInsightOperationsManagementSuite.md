---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531721"
---
# <span data-ttu-id="1c076-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="1c076-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="1c076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c076-102">SYNOPSIS</span></span>
<span data-ttu-id="1c076-103">HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하지 않도록 설정 하면 관련 로그가 사용 중에 지정 된 OMS 작업 영역으로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c076-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c076-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c076-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c076-105">DESCRIPTION</span></span>
<span data-ttu-id="1c076-106">**AzureRmHDInsightOperationsManagementSuite** Cmdlet은 Azure HDInsight 클러스터에서 OMS (Operations Management Suite)를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1c076-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c076-107">EXAMPLES</span></span>

### <span data-ttu-id="1c076-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c076-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="1c076-109">HDInsight 클러스터에서 OMS (Operations Management Suite)가 사용 되지 않도록 설정 되며 관련 로그가 OMS 작업 영역으로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="1c076-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c076-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="1c076-111">HDInsight 클러스터에서 OMS (Operations Management Suite)가 사용 되지 않도록 설정 되며 관련 로그가 OMS 작업 영역으로 이동 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="1c076-112">변수</span><span class="sxs-lookup"><span data-stu-id="1c076-112">PARAMETERS</span></span>

### <span data-ttu-id="1c076-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c076-113">-DefaultProfile</span></span>
<span data-ttu-id="1c076-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c076-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1c076-115">-Name</span></span>
<span data-ttu-id="1c076-116">OMS (Operations Management Suite)를 사용 하지 않도록 설정할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c076-117">-ResourceGroupName</span></span>
<span data-ttu-id="1c076-118">클러스터의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1c076-119">-Confirm</span></span>
<span data-ttu-id="1c076-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c076-121">-WhatIf</span></span>
<span data-ttu-id="1c076-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c076-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c076-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c076-124">CommonParameters</span></span>
<span data-ttu-id="1c076-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c076-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c076-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c076-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c076-127">입력</span><span class="sxs-lookup"><span data-stu-id="1c076-127">INPUTS</span></span>

### <span data-ttu-id="1c076-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1c076-128">System.String</span></span>

## <span data-ttu-id="1c076-129">출력</span><span class="sxs-lookup"><span data-stu-id="1c076-129">OUTPUTS</span></span>

### <span data-ttu-id="1c076-130">Microsoft. Azure. 관리 리소스</span><span class="sxs-lookup"><span data-stu-id="1c076-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="1c076-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1c076-131">NOTES</span></span>

## <span data-ttu-id="1c076-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c076-132">RELATED LINKS</span></span>

