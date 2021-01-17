---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492220"
---
# <span data-ttu-id="c197c-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c197c-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="c197c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c197c-102">SYNOPSIS</span></span>
<span data-ttu-id="c197c-103">애플리케이션 게이트웨이의 백 엔드 HTTP 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="c197c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c197c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c197c-105">설명</span><span class="sxs-lookup"><span data-stu-id="c197c-105">DESCRIPTION</span></span>
<span data-ttu-id="c197c-106">Get-AzApplicationGatewayBackendHttpSetting cmdlet은 애플리케이션 게이트웨이의 백 엔드 HTTP 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="c197c-107">예제</span><span class="sxs-lookup"><span data-stu-id="c197c-107">EXAMPLES</span></span>

### <span data-ttu-id="c197c-108">예제 1: 이름에 따라 백 엔드 HTTP 설정 확인</span><span class="sxs-lookup"><span data-stu-id="c197c-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="c197c-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 $AppGw Settings01이라는 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="c197c-110">예제 2: 백 엔드 HTTP 설정 컬렉션을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="c197c-111">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 $AppGw 대한 HTTP 설정 컬렉션을 $SettingsList 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="c197c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c197c-112">PARAMETERS</span></span>

### <span data-ttu-id="c197c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c197c-113">-ApplicationGateway</span></span>
<span data-ttu-id="c197c-114">백 엔드 HTTP 설정을 포함하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c197c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c197c-115">-DefaultProfile</span></span>
<span data-ttu-id="c197c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c197c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c197c-117">-Name</span></span>
<span data-ttu-id="c197c-118">이 cmdlet에서 얻을 백end HTTP 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c197c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c197c-119">CommonParameters</span></span>
<span data-ttu-id="c197c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c197c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c197c-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c197c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c197c-122">입력</span><span class="sxs-lookup"><span data-stu-id="c197c-122">INPUTS</span></span>

### <span data-ttu-id="c197c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c197c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c197c-124">출력</span><span class="sxs-lookup"><span data-stu-id="c197c-124">OUTPUTS</span></span>

### <span data-ttu-id="c197c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c197c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c197c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c197c-126">NOTES</span></span>

## <span data-ttu-id="c197c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c197c-127">RELATED LINKS</span></span>

[<span data-ttu-id="c197c-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c197c-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c197c-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c197c-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c197c-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c197c-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="c197c-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c197c-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

