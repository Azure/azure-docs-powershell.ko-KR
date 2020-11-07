---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 22B63259-799B-4F25-A06B-7A818D295870
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Reset-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 9ce8dc1faf1a762a847da5eb87fb28b510308054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703318"
---
# <span data-ttu-id="c4d21-101">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c4d21-101">Reset-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="c4d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d21-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d21-103">서버 관리 게이트웨이의 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-103">Resets the profile of a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c4d21-104">SYNTAX</span></span>

### <span data-ttu-id="c4d21-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c4d21-105">ByName</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4d21-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c4d21-106">ByObject</span></span>
```
Reset-AzureRmServerManagementGatewayProfile [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c4d21-107">DESCRIPTION</span></span>
<span data-ttu-id="c4d21-108">**AzureRmServerManagementGatewayProfile** Cmdlet은 Azure 서버 관리 게이트웨이의 프로필을 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-108">The **Reset-AzureRmServerManagementGatewayProfile** cmdlet resets the profile for an Azure Server Management Gateway.</span></span>

<span data-ttu-id="c4d21-109">프로필을 다시 설정한 후 프로필을 다운로드 하 고 Install-AzureRmServerManagementGatewayProfile cmdlet을 사용 하 여 저장 하려면 Save-AzureRmServerManagementGatewayProfile cmdlet을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-109">You will need to use the Save-AzureRmServerManagementGatewayProfile cmdlet to download the profile and then the Install-AzureRmServerManagementGatewayProfile cmdlet to save it after you reset the profile.</span></span>

## <span data-ttu-id="c4d21-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c4d21-110">EXAMPLES</span></span>

## <span data-ttu-id="c4d21-111">변수</span><span class="sxs-lookup"><span data-stu-id="c4d21-111">PARAMETERS</span></span>

### <span data-ttu-id="c4d21-112">-게이트웨이</span><span class="sxs-lookup"><span data-stu-id="c4d21-112">-Gateway</span></span>
<span data-ttu-id="c4d21-113">Cmdlet이 프로필을 다시 설정 하는 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-113">Specifies the gateway for which the cmdlet resets the profile for.</span></span>

<span data-ttu-id="c4d21-114">ResourceGoupName 및 게이트웨이 이름 대신 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-114">May be specified instead of ResourceGoupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d21-115">--게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="c4d21-115">-GatewayName</span></span>
<span data-ttu-id="c4d21-116">Cmdlet이 프로필을 다시 설정 하는 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-116">Specifies the name of the gateway for which the cmdlet resets the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d21-117">-ResourceGroupName</span></span>
<span data-ttu-id="c4d21-118">게이트웨이가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-118">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d21-119">-DefaultProfile</span></span>
<span data-ttu-id="c4d21-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4d21-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d21-121">CommonParameters</span></span>
<span data-ttu-id="c4d21-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d21-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d21-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d21-124">입력</span><span class="sxs-lookup"><span data-stu-id="c4d21-124">INPUTS</span></span>

### <span data-ttu-id="c4d21-125">게이트웨이와</span><span class="sxs-lookup"><span data-stu-id="c4d21-125">Gateway</span></span>
<span data-ttu-id="c4d21-126">' Gateway ' 매개 변수는 파이프라인에서 ' Gateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d21-126">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="c4d21-127">출력</span><span class="sxs-lookup"><span data-stu-id="c4d21-127">OUTPUTS</span></span>

## <span data-ttu-id="c4d21-128">상속자</span><span class="sxs-lookup"><span data-stu-id="c4d21-128">NOTES</span></span>

## <span data-ttu-id="c4d21-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4d21-129">RELATED LINKS</span></span>

[<span data-ttu-id="c4d21-130">설치-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c4d21-130">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="c4d21-131">저장-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c4d21-131">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


