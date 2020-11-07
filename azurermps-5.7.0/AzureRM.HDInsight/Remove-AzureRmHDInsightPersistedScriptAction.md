---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 08D1D6AC-D064-4E2D-9C22-0B65E7BE4DA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: 48b0fab43e104a5cae68ef26698735e89c603a78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703054"
---
# <span data-ttu-id="3b357-101">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3b357-101">Remove-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="3b357-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b357-102">SYNOPSIS</span></span>
<span data-ttu-id="3b357-103">HDInsight 클러스터에서 지속형 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-103">Removes an persisted script action from an HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b357-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b357-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [-Name] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b357-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3b357-105">DESCRIPTION</span></span>
<span data-ttu-id="3b357-106">**AzureRmHDInsightPersistedScriptAction** cmdlet은 지정 된 Azure HDInsight 클러스터의 지속형 스크립트 작업 목록에서 지속형 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-106">The **Remove-AzureRmHDInsightPersistedScriptAction** cmdlet removes a persisted script action from the specified Azure HDInsight cluster's list of persisted script actions.</span></span>
<span data-ttu-id="3b357-107">클러스터의 크기를 조정 하면 제거 된 스크립트도 더 이상 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-107">The removed script will no longer be executed when the cluster is scaled up.</span></span>

## <span data-ttu-id="3b357-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3b357-108">EXAMPLES</span></span>

### <span data-ttu-id="3b357-109">예제 1: 클러스터의 지속형 스크립트 작업 목록에서 스크립트 동작 제거</span><span class="sxs-lookup"><span data-stu-id="3b357-109">Example 1: Remove a script action from the list of persisted script actions on a cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightPersistedScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "Scriptaction"
```

<span data-ttu-id="3b357-110">이 명령은 지정 된 클러스터의 지속형 스크립트 작업 목록에서 Scriptaction 이라는 스크립트 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-110">This command removes the script action named Scriptaction from the list of persisted script actions on the specified cluster.</span></span>

## <span data-ttu-id="3b357-111">변수</span><span class="sxs-lookup"><span data-stu-id="3b357-111">PARAMETERS</span></span>

### <span data-ttu-id="3b357-112">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b357-112">-ClusterName</span></span>
<span data-ttu-id="3b357-113">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b357-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b357-114">-DefaultProfile</span></span>
<span data-ttu-id="3b357-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3b357-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b357-116">-이름</span><span class="sxs-lookup"><span data-stu-id="3b357-116">-Name</span></span>
<span data-ttu-id="3b357-117">제거할 지속형 스크립트 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-117">Specifies the name of the persisted script action to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b357-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b357-118">-ResourceGroupName</span></span>
<span data-ttu-id="3b357-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b357-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b357-120">CommonParameters</span></span>
<span data-ttu-id="3b357-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b357-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b357-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b357-123">입력</span><span class="sxs-lookup"><span data-stu-id="3b357-123">INPUTS</span></span>

### <span data-ttu-id="3b357-124">않아야</span><span class="sxs-lookup"><span data-stu-id="3b357-124">None</span></span>
<span data-ttu-id="3b357-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b357-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b357-126">출력</span><span class="sxs-lookup"><span data-stu-id="3b357-126">OUTPUTS</span></span>

### <span data-ttu-id="3b357-127">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="3b357-127">System.Void</span></span>

## <span data-ttu-id="3b357-128">상속자</span><span class="sxs-lookup"><span data-stu-id="3b357-128">NOTES</span></span>

## <span data-ttu-id="3b357-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b357-129">RELATED LINKS</span></span>

[<span data-ttu-id="3b357-130">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3b357-130">Get-AzureRmHDInsightPersistedScriptAction</span></span>](./Get-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="3b357-131">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="3b357-131">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)


