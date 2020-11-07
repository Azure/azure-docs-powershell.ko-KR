---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880194"
---
# <span data-ttu-id="f6f80-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="f6f80-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="f6f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f80-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f80-103">지정 된 풀의 운영 체제 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="f6f80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6f80-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f80-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6f80-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f80-106">**AzBatchPoolOSVersion** cmdlet은 지정 된 풀의 운영 체제 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="f6f80-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f6f80-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f80-108">예제 1: 풀의 대상 운영 체제 버전 설정</span><span class="sxs-lookup"><span data-stu-id="f6f80-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="f6f80-109">이 명령은 MyPool의 대상 운영 체제 버전을 WA-게스트-4.20 _201505-01로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="f6f80-110">변수</span><span class="sxs-lookup"><span data-stu-id="f6f80-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f80-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f6f80-111">-BatchContext</span></span>
<span data-ttu-id="f6f80-112">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f6f80-113">Get-AzBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f6f80-114">대신 공유 키 인증을 사용 하려면 Get-AzBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f6f80-115">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f6f80-116">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f80-117">-DefaultProfile</span></span>
<span data-ttu-id="f6f80-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f80-119">-Id</span><span class="sxs-lookup"><span data-stu-id="f6f80-119">-Id</span></span>
<span data-ttu-id="f6f80-120">풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6f80-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="f6f80-121">-TargetOSVersion</span></span>
<span data-ttu-id="f6f80-122">풀의 가상 컴퓨터에 설치할 Azure 게스트 운영 체제 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="f6f80-123">Azure 게스트 운영 체제 버전에 대 한 자세한 내용은 Azure 게스트 OS 릴리스 및 SDK 호환성 도표 https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="f6f80-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="f6f80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f80-124">CommonParameters</span></span>
<span data-ttu-id="f6f80-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6f80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f80-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f80-127">입력</span><span class="sxs-lookup"><span data-stu-id="f6f80-127">INPUTS</span></span>

### <span data-ttu-id="f6f80-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f6f80-128">System.String</span></span>

### <span data-ttu-id="f6f80-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f6f80-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f6f80-130">출력</span><span class="sxs-lookup"><span data-stu-id="f6f80-130">OUTPUTS</span></span>

### <span data-ttu-id="f6f80-131">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="f6f80-131">System.Void</span></span>

## <span data-ttu-id="f6f80-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f6f80-132">NOTES</span></span>

## <span data-ttu-id="f6f80-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6f80-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6f80-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f6f80-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


