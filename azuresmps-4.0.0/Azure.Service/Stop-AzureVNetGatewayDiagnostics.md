---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046019"
---
# <span data-ttu-id="cef46-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="cef46-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="cef46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cef46-102">SYNOPSIS</span></span>
<span data-ttu-id="cef46-103">실행 중인 VPN 게이트웨이 진단 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="cef46-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cef46-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cef46-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cef46-105">DESCRIPTION</span></span>
<span data-ttu-id="cef46-106">**Stop-Azurevnet2| 진단** cmdlet은 실행 중인 가상 개인 네트워크 (VPN) 게이트웨이 진단 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="cef46-107">이 명령은 진단 세션의 결과를 시작 하 고 **Azurevnet2| 진단** cmdlet이 지정 하는 저장소 계정에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="cef46-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cef46-108">EXAMPLES</span></span>

## <span data-ttu-id="cef46-109">변수</span><span class="sxs-lookup"><span data-stu-id="cef46-109">PARAMETERS</span></span>

### <span data-ttu-id="cef46-110">-프로필</span><span class="sxs-lookup"><span data-stu-id="cef46-110">-Profile</span></span>
<span data-ttu-id="cef46-111">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cef46-112">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef46-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="cef46-113">-VNetName</span></span>
<span data-ttu-id="cef46-114">이 cmdlet이 진단을 중지 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cef46-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef46-115">CommonParameters</span></span>
<span data-ttu-id="cef46-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cef46-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef46-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef46-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef46-118">입력</span><span class="sxs-lookup"><span data-stu-id="cef46-118">INPUTS</span></span>

## <span data-ttu-id="cef46-119">출력</span><span class="sxs-lookup"><span data-stu-id="cef46-119">OUTPUTS</span></span>

## <span data-ttu-id="cef46-120">상속자</span><span class="sxs-lookup"><span data-stu-id="cef46-120">NOTES</span></span>

## <span data-ttu-id="cef46-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cef46-121">RELATED LINKS</span></span>

[<span data-ttu-id="cef46-122">Get-Azurevnet게이트웨이 진단</span><span class="sxs-lookup"><span data-stu-id="cef46-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="cef46-123">Start-Azurevnet2| 진단</span><span class="sxs-lookup"><span data-stu-id="cef46-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


