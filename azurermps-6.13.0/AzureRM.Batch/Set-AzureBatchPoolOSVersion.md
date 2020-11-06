---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: d85e0ca61b86e523c6d73ea8d2349d7d692aafb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533431"
---
# <span data-ttu-id="73bab-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="73bab-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="73bab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bab-102">SYNOPSIS</span></span>
<span data-ttu-id="73bab-103">지정 된 풀의 운영 체제 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73bab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73bab-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73bab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73bab-105">DESCRIPTION</span></span>
<span data-ttu-id="73bab-106">**AzureBatchPoolOSVersion** cmdlet은 지정 된 풀의 운영 체제 버전을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="73bab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73bab-107">EXAMPLES</span></span>

### <span data-ttu-id="73bab-108">예제 1: 풀의 대상 운영 체제 버전 설정</span><span class="sxs-lookup"><span data-stu-id="73bab-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="73bab-109">이 명령은 MyPool의 대상 운영 체제 버전을 WA-게스트-4.20 _201505-01로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="73bab-110">변수</span><span class="sxs-lookup"><span data-stu-id="73bab-110">PARAMETERS</span></span>

### <span data-ttu-id="73bab-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="73bab-111">-BatchContext</span></span>
<span data-ttu-id="73bab-112">이 cmdlet이 일괄 처리 서비스와 상호 작용 하는 데 사용 하는 **Batchaccountcontext** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="73bab-113">Get-AzureRmBatchAccount cmdlet을 사용 하 여 BatchAccountContext를 가져오는 경우, 일괄 서비스와 상호 작용할 때 Azure Active Directory 인증이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="73bab-114">대신 공유 키 인증을 사용 하려면 Get-AzureRmBatchAccountKeys cmdlet을 사용 하 여 선택 키가 채워진 BatchAccountContext 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="73bab-115">공유 키 인증을 사용 하는 경우 기본 선택 키가 기본적으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="73bab-116">사용할 키를 변경 하려면 BatchAccountContext 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="73bab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bab-117">-DefaultProfile</span></span>
<span data-ttu-id="73bab-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73bab-119">-Id</span><span class="sxs-lookup"><span data-stu-id="73bab-119">-Id</span></span>
<span data-ttu-id="73bab-120">풀의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-120">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="73bab-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="73bab-121">-TargetOSVersion</span></span>
<span data-ttu-id="73bab-122">풀의 가상 컴퓨터에 설치할 Azure 게스트 운영 체제 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="73bab-123">Azure 게스트 운영 체제 버전에 대 한 자세한 내용은 Azure 게스트 OS 릴리스 및 SDK 호환성 도표 https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (을 참조 하세요 https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="73bab-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="73bab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bab-124">CommonParameters</span></span>
<span data-ttu-id="73bab-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73bab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bab-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bab-127">입력</span><span class="sxs-lookup"><span data-stu-id="73bab-127">INPUTS</span></span>

### <span data-ttu-id="73bab-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73bab-128">System.String</span></span>

### <span data-ttu-id="73bab-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="73bab-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="73bab-130">매개 변수: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="73bab-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="73bab-131">출력</span><span class="sxs-lookup"><span data-stu-id="73bab-131">OUTPUTS</span></span>

### <span data-ttu-id="73bab-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="73bab-132">System.Void</span></span>

## <span data-ttu-id="73bab-133">상속자</span><span class="sxs-lookup"><span data-stu-id="73bab-133">NOTES</span></span>

## <span data-ttu-id="73bab-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73bab-134">RELATED LINKS</span></span>

[<span data-ttu-id="73bab-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="73bab-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


