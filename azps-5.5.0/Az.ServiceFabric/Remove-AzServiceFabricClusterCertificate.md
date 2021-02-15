---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197828"
---
# <span data-ttu-id="57e3c-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="57e3c-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="57e3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e3c-102">SYNOPSIS</span></span>
<span data-ttu-id="57e3c-103">클러스터 보안에 사용되는 클러스터 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="57e3c-104">구문</span><span class="sxs-lookup"><span data-stu-id="57e3c-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57e3c-105">설명</span><span class="sxs-lookup"><span data-stu-id="57e3c-105">DESCRIPTION</span></span>
<span data-ttu-id="57e3c-106">클러스터에 이미 사용 중인 다른 유효한 인증서가 있는 한 **Remove-AzServiceFabricClusterCertificate를** 사용하여 클러스터에서 클러스터 인증서를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="57e3c-107">예제</span><span class="sxs-lookup"><span data-stu-id="57e3c-107">EXAMPLES</span></span>

### <span data-ttu-id="57e3c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="57e3c-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="57e3c-109">이 명령은 지문이 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A인 인증서를 클러스터 보안에 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="57e3c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57e3c-110">PARAMETERS</span></span>

### <span data-ttu-id="57e3c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e3c-111">-DefaultProfile</span></span>
<span data-ttu-id="57e3c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e3c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="57e3c-113">-Name</span></span>
<span data-ttu-id="57e3c-114">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e3c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e3c-115">-ResourceGroupName</span></span>
<span data-ttu-id="57e3c-116">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57e3c-117">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="57e3c-117">-Thumbprint</span></span>
<span data-ttu-id="57e3c-118">제거할 클러스터 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57e3c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57e3c-119">-Confirm</span></span>
<span data-ttu-id="57e3c-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57e3c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57e3c-121">-WhatIf</span></span>
<span data-ttu-id="57e3c-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57e3c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57e3c-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57e3c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e3c-124">CommonParameters</span></span>
<span data-ttu-id="57e3c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57e3c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e3c-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57e3c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e3c-127">입력</span><span class="sxs-lookup"><span data-stu-id="57e3c-127">INPUTS</span></span>

### <span data-ttu-id="57e3c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="57e3c-128">System.String</span></span>

## <span data-ttu-id="57e3c-129">출력</span><span class="sxs-lookup"><span data-stu-id="57e3c-129">OUTPUTS</span></span>

### <span data-ttu-id="57e3c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="57e3c-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="57e3c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57e3c-131">NOTES</span></span>

## <span data-ttu-id="57e3c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57e3c-132">RELATED LINKS</span></span>
