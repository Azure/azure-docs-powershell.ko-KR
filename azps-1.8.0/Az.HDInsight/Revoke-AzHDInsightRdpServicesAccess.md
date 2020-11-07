---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868210"
---
# <span data-ttu-id="b5c62-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b5c62-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="b5c62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c62-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c62-103">Windows 클러스터에 대 한 RDP 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="b5c62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5c62-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5c62-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c62-106">**AzHDInsightRdpServicesAccess** Cmdlet은 Windows 기반 Azure HDInsight 클러스터에 대 한 RDP (원격 데스크톱 프로토콜) 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b5c62-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5c62-107">EXAMPLES</span></span>

### <span data-ttu-id="b5c62-108">예제 1: 지정 된 클러스터에 대 한 RDP 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="b5c62-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b5c62-109">이 명령은-hadoop-001 이라는 클러스터에 대 한 RDP 액세스를 해지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b5c62-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5c62-110">PARAMETERS</span></span>

### <span data-ttu-id="b5c62-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b5c62-111">-ClusterName</span></span>
<span data-ttu-id="b5c62-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c62-113">-DefaultProfile</span></span>
<span data-ttu-id="b5c62-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b5c62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5c62-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c62-115">-ResourceGroupName</span></span>
<span data-ttu-id="b5c62-116">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5c62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c62-117">CommonParameters</span></span>
<span data-ttu-id="b5c62-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5c62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c62-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c62-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c62-120">입력</span><span class="sxs-lookup"><span data-stu-id="b5c62-120">INPUTS</span></span>

### <span data-ttu-id="b5c62-121">않아야</span><span class="sxs-lookup"><span data-stu-id="b5c62-121">None</span></span>

## <span data-ttu-id="b5c62-122">출력</span><span class="sxs-lookup"><span data-stu-id="b5c62-122">OUTPUTS</span></span>

### <span data-ttu-id="b5c62-123">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b5c62-123">System.Void</span></span>

## <span data-ttu-id="b5c62-124">상속자</span><span class="sxs-lookup"><span data-stu-id="b5c62-124">NOTES</span></span>

## <span data-ttu-id="b5c62-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5c62-125">RELATED LINKS</span></span>

[<span data-ttu-id="b5c62-126">부여-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b5c62-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


